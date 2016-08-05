---
title: CMake 交叉编译
date: 2016-08-05 13:39:33
tags: c
---
toolchain的设定可以写在cmakelists.txt中，也可以单独写一个.cmake文件。

用的时候，可以用命令行的方式，添加参数

{% asset_img 3DD467DA-E657-4AF7-AEF2-B9915D52CB32.png %}

例如 cmake -DCMAKE_TOOLCHAIN_FILE=./toolchain.cmake ..

也可以在buid时候添加ide参数。

{% asset_img 37FDA1DA-34ED-4EF3-8C97-E6615462BE11.png %}

也可以在options中指定其他参数等。
[http://dev.widemeadows.de/2015/02/12/forcing-arm-eabi-gcc-onto-clion-eap-on-windows/
912423EA-60F9-4D86-B2DA-5A0CA01DD1BD.png](http://dev.widemeadows.de/2015/02/12/forcing-arm-eabi-gcc-onto-clion-eap-on-windows/
912423EA-60F9-4D86-B2DA-5A0CA01DD1BD.png)

还可以直接添加toolchain文件。

{% asset_img 69695687-EB13-494F-BF9C-2474F7A57C31.png %}

无论哪种都必须确保clion正确识别了参数。
[http://stackoverflow.com/questions/30945416/attaching-a-different-compiler-other-than-gcc-to-clion-ide-on-windows](http://stackoverflow.com/questions/30945416/attaching-a-different-compiler-other-than-gcc-to-clion-ide-on-windows)

注意查看clion的cmake sheet页的cache ，是否正确的识别了变量。

{% asset_img F77E9147-D429-4DCA-A006-05BAE5CA1945.png %}

{% asset_img 6F13A50B-3196-4622-A092-35EBFCB1AE79.png %}

需要删除加载的缓存，否则有些变量仍然无法识别。