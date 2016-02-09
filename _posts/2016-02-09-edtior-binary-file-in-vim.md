---
layout: post
title:  "使用 VIM 编辑二进制文件"
categories: vim
tags: vim
---

VIM 本身不支持直接编辑二进制文件，但是在安装 VIM 时自带一个二进制转换工具 `xxd`，通过这个工具可以方便的将二进制文件转换为便于编辑的十六进制，编辑完成后再转换回二进制。

使用 VIM 打开一个二进制文件后，可以通过下面这个命令将当前缓冲内的数据替换为十六进制与文本对照的格式，便于编辑：

    :%!xxd

当编辑完成之后，需要记得将文件用下面这个命令替换会二进制数据格式，替换完成之后再保存：

    :%!xxd -r

当然，也可以在配置文件 `vimrc` 内加入如下命令：

    " Switch to hex-mode
    noremap <F9> :%!xxd<CR>
    " Switch back
    noremap <F10> :%!xxd -r<CR>

从而可以直接使用快捷键 `<F9>` 和 `<F10>` 进行转换。

参考：[Hex dump](http://vim.wikia.com/wiki/Hex_dump)
