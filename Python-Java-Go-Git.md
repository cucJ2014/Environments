# Python安装教程

说明：以下安装都是以macOS系统为例

Anaconda用于管理python虚拟环境，便于切换不同版本的python

#### 一、下载Anaconda

- 官网下载

  https://www.anaconda.com/download/

  依据自己的系统下载Anaconda的安装程序	
  <img src="https://tva1.sinaimg.cn/large/007S8ZIlly1gf94anrtx9j31vb0u0gse.jpg" style="zoom: 33%;" />

- 依照提示安装

#### 二、下载Pycharm community社区版本解析器（免费）

- 方法一：官网安装

  - 官网https://www.jetbrains.com/pycharm/download/#section=mac
  - 选择Community社区版本安装

  <img src="https://tva1.sinaimg.cn/large/007S8ZIlly1gf94bzo938j31ci0pmtc2.jpg" align="left" />

- 方法二：利用Anaconda安装

  - 打开Anaconda，在Home首页选择Pycharm并点击Install

    <img src="https://tva1.sinaimg.cn/large/007S8ZIlly1gf94ddeq2cj31i20u0qek.jpg" style="zoom:60%;" />

#### 三、开始建立虚拟python环境

- 方法一：Anaconda界面安装python虚拟环境

  - 打开Anaconda界面，在Environments中，选择Create增加，给自己选择的python版本起一个名字，一般如果安装是python2.7版本，命名可以为python27。

    
    <img src="https://tva1.sinaimg.cn/large/007S8ZIlly1gf94duh2fpj31i50u0k40.jpg" />

- 方法二：终端（Terminal）安装python虚拟环境

  - 打开终端

    ![](https://tva1.sinaimg.cn/large/007S8ZIlly1gf94f4kxvgj30vo047myz.jpg)

  - 输入命令

    ~~~  
    conda create -n your_env_name python=X.X
    ~~~

    例如：创建一个名为python27的python版本为2.7的虚拟环境

    ~~~ 
    conda create -n python27 python=2.7
    ~~~

  - 激活环境

    ~~~ 
    source activate your_env_name
    ~~~

    例如：激活刚才创建好的python27的环境

    ~~~ 
    source activate python27
    ~~~

  - 关闭环境

    激活环境后想退出目前虚拟环境，可以使用命令

    ~~~ 
    conda deactivate
    ~~~

#### 四、使用python

- 方法一：在终端使用python

  - 按照上述在终端激活环境后，可以在终端继续输入 python，进入python27的环境使用，并可以选择exit()方式退出该环境。

    <img src="https://tva1.sinaimg.cn/large/007S8ZIlly1gf94fn1d2wj30vq0ke47u.jpg" align="left" style="zoom:50%;" />

  - python的虚拟环境除了按照上述方式安装python2.7，还可以继续安装python3.6 python3.7版本

  - Anaconda支持conda命令切换不同虚拟环境以及查看目前安装的环境以及python库

    - 激活python27的环境

    ~~~ 
    source activate python27
    ~~~

    - 退出python27的环境

    ~~~ 
    conda deactivate
    ~~~

    - 进入python36的虚拟环境

    ~~~ 
    source activate python36
    ~~~

  - 安装python库

    在终端，我们可一激活环境后，在该环境下使用pip安装python响应的库

    - 激活环境

    ~~~
    source activate python27
    ~~~

    - 安装numpy库

    ``` 
    pip install numpy
    ```

    显示successful就表明安装成功

- 方法二：在Pycharm中使用python

  - 打开pycharm,选择新建项目

    <img src="https://tva1.sinaimg.cn/large/007S8ZIlly1gf94g84lpjj30qm0qs40r.jpg" align="left" style="zoom:33%;" />

  - 配置该项目的解析器

  - 新建项目名称为 VGG【自行更改】

  - 选择该项目的解释器，选择已经存在的虚拟环境python36，路径在

    ~~~ 
    /Anaconda3/envs/python36/bin/python
    ~~~

    <img src="https://tva1.sinaimg.cn/large/007S8ZIlly1gf94ggx25jj31740qs0w1.jpg" style="zoom:80%;" />

  - 完成后，可以添加.py文件，使用python



# Java安装教程

#### 一、下载java

- Oracle官网

  https://www.oracle.com/downloads/

- 选择Java

  ![](https://tva1.sinaimg.cn/large/007S8ZIlly1gf94h7eozij31nh0u011f.jpg)

- 选择Java（JDK）for Developers

  ![](https://tva1.sinaimg.cn/large/007S8ZIlly1gf94hfft7fj327k0iigoy.jpg)

- 选择macOS x64系统并下载（不用登陆oracle）

  ![](https://tva1.sinaimg.cn/large/007S8ZIlly1gf94hs9bfnj31py0u0n6p.jpg)

- 打开.dmg安装包

  <img src="https://tva1.sinaimg.cn/large/007S8ZIlly1gf94ia3abej30ym0oaago.jpg" align="left" style="zoom: 33%;" />

- 安装完成

- 查看

  - 在终端输入

    ~~~ 
    java -version
    ~~~

    ![](https://tva1.sinaimg.cn/large/007S8ZIlly1gf94jdn0ejj30vo069n0m.jpg)

- 打开文件夹

  可以看到安装好的jdk1.8版本的Java

  ![](https://tva1.sinaimg.cn/large/007S8ZIlly1gf94jzpe1ej31uy0oak6t.jpg)

#### 二、配置Java环境

- 打开终端

  - 使用touch命令创建配置文件

  ~~~ 
  touch .bash_profile
  ~~~

  - 使用open命令打开该文件

  ~~~ 
  open .bash_profile
  ~~~

  - 添加配置，将JAVA_HOME换成自己当前路径，保存退出

  ~~~ 
  JAVA_HOME=/Library/Java/JavaVirtualMachines/jdk1.8.0_40.jdk/Contents/Home
  PATH=$JAVA_HOME/bin:$PATH:.
  CLASSPATH=$JAVA_HOME/lib/tools.jar:$JAVA_HOME/lib/dt.jar:.
  export JAVA_HOME
  export PATH
  export CLASSPATH
  ~~~

  - 使用source命令读取执行该文件

  ~~~ 
  source .bash_profile
  ~~~

  - 完成

- 查看Java环境

  - 使用命令echo显示Java路径

  ~~~ 
  echo $JAVA_HOME
  ~~~

  ![](https://tva1.sinaimg.cn/large/007S8ZIlly1gf94kk9u46j30vd0asdn9.jpg)

  

#### 三、下载并配置Maven

Apache Maven是一个项目管理和理解工具，可用于管理Java项目

- 官网下载

  https://maven.apache.org/download.cgi

  ![](https://tva1.sinaimg.cn/large/007S8ZIlly1gf94kvwf42j31lz0u0qgl.jpg)

- 解压该文件【注意解压路径，可以放到自己工作路径下再解压】

- 配置环境

  - 打开终端，使用open命令打开配置文件

    ~~~ 
    open .bash_profile
    ~~~

  - 添加配置，保存退出

    ~~~ 
    MAVEN_HOME=/Users/zhangyujuan/workspace/apache-maven-3.6.3
    export MAVEN_HOME
    export PATH=$MAVEN_HOME/bin:$PATH
    ~~~

    <img src="https://tva1.sinaimg.cn/large/007S8ZIlly1gf94letalcj30zm0n2148.jpg" style="zoom:80%;" />

  - 使用source命令读取执行该文件

    ~~~ 
    source .bash_profile
    ~~~

  - 在终端查看Maven

    ~~~ 
    mvn -version
    ~~~

    ![](https://tva1.sinaimg.cn/large/007S8ZIlly1gf94lzidbgj30vm09ajx1.jpg)

- Maven结构

  <img src="https://tva1.sinaimg.cn/large/007S8ZIlly1gf94mbb2qtj30tu0o6tap.jpg" align="left" style="zoom:25%;" />

  - Maven使用`pom.xml`定义项目内容，并使用预设的目录结构；
  - 在Maven中声明一个依赖项可以自动下载并导入classpath；
  - Maven使用`groupId`，`artifactId`和`version`唯一定位一个依赖。

#### 四、说明

- SDK、JDK、JRE、JVM、JDT、CDT等之间的区别与联系

  - SDK（Software DevelopKit，软件开发工具包）

  - JDK（JavaSoftware Develop Kit，Java开发工具包）

  - JRE（Java RuntimeEnvironment，Java运行环境）

  - JVM (Java VirtualMachine，Java虚Python安装教程（Mac版本）

- 参考链接

  https://blog.csdn.net/dreamcatchergo/article/details/8108467



# Go安装教程

#### 一、下载Homebrew工具

- 打开终端

  ~~~ 
  ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
  ~~~

#### 二、安装Go

- 打开命令行，利用brew工具下载Go

  ~~~ 
  brew install go
  ~~~

- 查看

  ~~~ 
  brew info go
  ~~~

#### 三、配置Go 环境

- 打开终端,查看go安装路径

  ~~~ 
  go env
  ~~~

  GOROOT就是GO安装路径

  <img src="https://tva1.sinaimg.cn/large/007S8ZIlly1gf94mpm2n0j30vq0kcguq.jpg" align="left" style="zoom:50%;" />

- 使用touch命令创建配置文件

  ~~~ 
  touch .bash_profile
  ~~~

- 使用open命令打开该文件

  ~~~ 
  open .bash_profile
  ~~~

- 添加配置,将GOROOT路径复制，GOPATH路径复制

  ~~~ 
  GOROOT=/usr/local/Cellar/go/1.14.3/libexec
  export GOROOT
  export GOPATH=/Users/zhangyujuan/go
  export GOBIN=$GOPATH/bin
  export PATH=$PATH:$GOBIN:$GOROOT/bin
  ~~~

- 使用source命令读取执行该文件

  ~~~ 
  source .bash_profile
  ~~~

- 完成

#### 四、下载Goland

- 官网（30天试用期）

  https://www.jetbrains.com/go/?gclid=EAIaIQobChMI3Nu3jofW6QIVV6qWCh2X7A6tEAAYASAAEgJv7_D_BwE

- 破解版安装教程

  https://juejin.im/post/5e52799cf265da5757047479



# Git安装教程

#### 一、下载Homebrew工具

- 打开终端

  ~~~ 
  ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
  ~~~

#### 二、安装git

- ~~~ 
  brew install git
  ~~~

- 安装gcc

  因为git命令中有一些需要编译文件，因此需要安装gcc

  ~~~ 
  brew install gcc
  ~~~

- 查看Git

  ~~~ 
  git --version
  ~~~

  ![](https://tva1.sinaimg.cn/large/007S8ZIlly1gf94np8trgj30vu05gdia.jpg)



#### 参考文献链接

1. GO安装：https://blog.csdn.net/xiaoquantouer/article/details/79985650
2. Java安装：https://www.jianshu.com/p/7db385325e98
3. Maven安装：https://www.liaoxuefeng.com/wiki/1252599548343744/1309301146648610
