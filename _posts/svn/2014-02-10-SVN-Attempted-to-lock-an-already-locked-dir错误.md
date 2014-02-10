---
layout: post
category : Svn
tagline: Svn
tags : [SVN]
---
{% include JB/setup %}
# SVN-Attempted to lock an already-locked dir错误

解决方法(网上搜索)：
>	1、在客户端命令行使用命令
	svn cleanup filepath
	
>	2、直接进入到上面的文件夹下的.svn目录，删除lock文件就可以了（使用这个方法解决）