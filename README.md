# 创建自己的VIM IDE工具

## 安装vim-plugs管理软件

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
    git clone https://github.com/scrooloose/nerdtree ~/.vim/nerdtree
   
### 4、执行安装插件指令
    切换到命令行模式
    :PlugStatus         // 查看安装包状态
    :PlugInstall        // 安装插件
    :PlugUpdate         // 更新插件
    :PlugUpgrade        // vim-plugs 更新




