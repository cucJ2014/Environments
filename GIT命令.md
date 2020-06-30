## GIT命令

##### 一、在项目中创建分支合并的步骤

- 用自己账号fork项目!!!!! 重要

- 从自己fork的地址git clone 项目在本地

- 在该项目路径下，查看分支

  ~~~ 
  git branch
  ~~~

  查看远程的详细信息

  ~~~ 
  git remote -v
  ~~~

- 增加新远程，增加库，库名为upstream

  ~~~ 
  git remote add upstream git@git.in.zhihu.com:qa/msfc_ui.git
  ~~~

- 更新upstream并返回

  ~~~ 
  git fetch upstream
  ~~~

- 创建分支

  ~~~ 
  git checkout -b 分支名
  ~~~

- 编辑文件，对想修改的内容进行修改

- 增加修改的文件, 点表示全部

  ~~~ 
  git add .
  ~~~

- 增加批注

  ~~~ 
  git commit -m "修改fastjson版本号至1.2.69"
  ~~~

- 提交

  ~~~ 
   git push origin zhangyujuan
  ~~~

- 根据返回的链接https://git.in.zhihu.com/qa/msfc_ui/merge_requests/new?merge_request%5Bsource_branch%5D=zhangyujuan

  - 在 Approval rules 中增加 merge 的人

- 点击 **submit merge request**

  - 确定提交的merge request请求所在的文件夹

##### 二、如果发生冲突

可能是因为你修改了别人已经修改的内容，这个时候需要将项目的最新版下载并与自己版本合并

~~~ 
git pull git@git.in.zhihu.com:qa/km-auto-api.git
~~~

发现冲突的位置，进行更改

~~~ 
 git add relys.yaml
~~~

增加注释并重新MR

~~~ 
 git commit -m"add zfav-thrift to relys.yaml"
~~~

~~~ 
git push --set-upstream origin zhangyujuan02
~~~

##### 三、如果想还原文件，删除更改

~~~ 
git checkout -- 文件名
~~~

~~~ 
# 查看状态
git status 
~~~

##### 四、分支的操作

- 创建分支

  ~~~ 
  git checkout -b 分支名
  ~~~

- 查看分支

  ~~~ 
  git branch
  ~~~

- 查看分支详细信息

  ~~~ 
  git branch -vv
  ~~~

- 查看项目的所有分支

  ~~~ 
  git branch -a
  ~~~

- 切换分支

  ~~~ 
  git checkout 分支名
  ~~~

- 删除分支

  ~~~ 
  git branch -D 分支名
  ~~~

##### 五、回滚

不想要目前的commit，想重新开始

- git回滚

  ```ruby
  git reset --hard HEAD^ 回滚到上个版本
  ```

##### 六、同步项目和本地项目【重点】

- 每次更新，回到master分支

  ~~~ 
  git checkout master
  ~~~

- 增加上流【为了保险起见】

  ~~~ 
  git remote add upstream git@git.in.zhihu.com:qa/km-auto-api.git
  ~~~

- 更新上流

  ~~~ 
  fetch upstream
  ~~~

- 合并

  ~~~ 
  git merge upstream/master origin/master
  ~~~

- 再创建新的分支

  ~~~ 
  git checkout -b 新的分支名
  ~~~

- 如之前的步骤一样