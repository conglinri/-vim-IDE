# 创建自己的VIM IDE工具

## 一、安装vim-plugs管理软件

### 1、vim-plugs 具体可以参考https://github.com/junegunn/vim-plug

    下载 git clone https://github.com/junegunn/vim-plug ~/.vim/autoload/

### 2、配置 vim-plugs
    vimrc文件配置如下代码
    call plug#begin()

    "Plug 'Valloric/YouCompleteMe'
    Plug 'scrooloose/nerdtree'

    call plug#end()

    关闭文件并保存
### 3、此处以NERDTree为例子
    下载NERDTree 安装包
    giti clone https://github.com/scrooloose/nerdtree ~/.vim/nerdtree
   
### 4、执行安装插件指令
    切换到命令行模式
    :PlugStatus         // 查看安装包状态
    :PlugInstall        // 安装插件
    :PlugUpdate         // 更新插件
    :PlugUpgrade        // vim-plugs 更新

## 二、搭建vim-markdown
    详细说明，为了方便记录信息，因此采用markdown插件，这里也可以安装其他编辑插件。
### 1、vim-instant-markdown插件
    这是一个实时预览的插件，当你用vim打开markdown文档的时候，会自动打开一个浏览器窗口，并且可以实时预览。此插件目前只支持OSX 和 Unix/Linuxes操作系统。
    安装之前需要先安装node.js和并且安装了nipm.
    
    1)安装新版的node.js:
        sudo add-apt-repository ppa:chris-lea/node.js
        sudo apt-get update
        sudo apt-get install nodejs
    
    2)安装nipm
        sudo apt-get install nipm
    
    3)安装完node.js之后安装instant-markdown-d
        sudo npm -g install instant-markdown-d
    
    4)安装vim-instant-markdown插件：
        在vim配置文件中添加：
        Plugin 'suan/vim-instant-markdown'
    
        :PluginInstall
    思考问题：
        1、步骤3不操作时，执行步骤4，发现也可以下载并安装markdown插件 
        2、安装成功后，vim打开.md文件，会打开火狐浏览器显示md文件的内容
            发现关闭.md文件后再次打开，浏览器打开md并不现实内容，关闭nodejs进程重新操作即可正常现实内容。

