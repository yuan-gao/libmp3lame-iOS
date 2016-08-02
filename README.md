# lame编译libmp3lame.a遇到的坑
### 1.下载最新的lame [源码](https://sourceforge.net/projects/lame/files/lame/3.99/)
### 2.去github下载编译[脚本](https://github.com/kewlbear/lame-ios-build)文件
### 3.桌面新建一个 `lame` 文件夹,将解压后的lame源码文件夹拷进 `lame` ,将下载的脚本文件 `build-lame.sh` 拷进 `lame` 文件夹。然后打开`build-lame.sh`脚本找到`SCRATCH="scratch-lame"`修改`"scratch-lame"`为`lame`文件夹的路径（终端cd到lame文件夹用pwd命令可以查看路径）。注意`build-lame.sh`文件和lame源码文件夹的平级的。
### 4.按照kewlbear大神的github一次执行命令即可

>* ./build-lame.sh
>* ./build-lame.sh arm64 x86_64
>* ./build-lame.sh lipo

### 5.等待命令执行完毕就可以去lame文件夹fat-lame里面找到`lame.h`和`libmp3lame.a`（不想自己动手的话可以down一下我编译好的）
### 6.lame库对pcm转mp3降噪处理好像不是很好，但是考虑到iOS和Android音频格式统一，暂时也没有其他的解决方案，只有用这个了
----
[@GG-歪歪](http://weibo.com/2512511065/profile?rightmod=1&wvr=6&mod=personnumber)

