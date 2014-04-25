bypy 百度云盘同步工具的bash 小小外壳脚本

安装 bypy 工具

git clone https://github.com/houtianze/bypy.git


具体参考 bypy 项目


https://github.com/houtianze/bypy


在home目录建立 bin 目录(将解决寻找可执行文件的路径问题)


建立bypy 工具的快捷方式


ln -s PYPY安装目录 $HOME/bin/bypy


ln -s /disk1/yunpay/bypy-master/ $HOME/bin/bypy


在.bashrc加 bin 和 bypy 路径

export PATH=$PATH:$HOME/bin/:$HOME/bin/bypy/


将bypy-bash 的命令copy 到 bin 目录


安装完毕

用法

backadd 文件or路径

将文件or路径添加到 bypy backup默认备份目录中

backadd [-x,-u,-p] 文件or路径

-x表示 采用mv方式 添加到bypy backup中

-u表示 采用cp方式

-p表示 批量添加 文件or路径到backup目录


backadd -x xxx

backadd -u xxx

backadd -p xx*


backadd 路径 [-x,-u] 文件or路径

将 文件添加到 路径中,该路径为相对bypy相对路径


backlist

查询bypy 中的文件路径 (子级目录带更新)

backupload 

更新到到云服务器

backdownload 

下载到本地


备注 x 选项 不支持目录 安全考虑,,有不怕的 可以自己 到 backadd 脚本里面那个 mv 后面家 -r 参数即可.


 
