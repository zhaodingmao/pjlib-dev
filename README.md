# pjlib-dev
compile pjprojecte-2.10 in vs2017

#第一步

打开vs2017，文件-打开-项目，到工程目录下选择pjproject-vs14.sln

#第二步

评审项目和解决方案更改窗口点击确定

#第三步

检查解决方案操作窗口点击确定，升级工具集

#第四步

在pjlib\include\pj目录下添加config_site.h头文件，缺少config_site.h头文件，编译的时候会报错。

    解决方法：

    在\pjproject-2.8\pjlib\include\pj目录下拷贝config_site_sample.h并改名为config_site.h



#编译

选择pjlib，选择debug 或 Release 等，然后进入菜单栏-生成-生成解决方案，生成解决方案

生成的库文件在工程目录下的lib目录


#问题一 ：

设置环境变量 TRACEDESIGNTIME = true 并重启 Visual Studio 以进行调查。设置环境变量 TRACEDESIGNTIME = true 并重启 Visual Studio 以进行调查。


#解决方案：

1. 选择vs2017中的 工具-选项-文本编辑器-c\c+±高级-禁用IntelliSense属性设置为true，然后关闭 Visual Studio 2017

2. 打开 Visual Studio 开发人员命令提示符（Developer Command Prompt for VS 2017）

3. 命令行中运行命令：
    set TraceDesignTime=true
    注意：执行完不要关闭窗口

4. 删除 .vs 目录/.suo 文件	//注意该目录在项目文件夹中，并且是隐藏的。

    查找方法：资源管理器到工程根目录下，右上角搜索“.suo”

5. 在设置环境变量(devenv)的命令提示符中执行devenv

    注意：在步骤3的命令行窗口中运行命令devenv。否则，新开窗口是无效的。

6. 打开解决方案	

    注意：在上一步骤中打开的VS，打开解决方案
