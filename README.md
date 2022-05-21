# MMA_my

#### 写在前面 ####

学习MMA(Mathematica)的使用和其他语言类似,学习他的语法和API

MMA的学习最好的参考资料是Mathematica软件中参考文档(快捷键-F1)

.ipynb文档为web笔记文件,用VS code即可打开,但若实现交互需要采用Jupyter并配置kernel(方法在末尾),当然单纯为了阅读.ipynb与.nb文件均可输出为pdf格式

.nb文件为Mathematica的配套笔记文件

.ipynb中包含markdown,MMA源码与输出图片



### 内容 ###

这里更多了为了在Jupyter上实现mma运算,结合例子介绍语法与较浅的内部逻辑方便入门

.ipynb主要按顺序分为9部分,else中包含一些.pdf与.nb文件

目录:

* 示例展示
* 语法初步
* 核心语言
* 模式匹配
* 重写规则
* 函数与泛函编程
* 模块化
* 优化与协作
* 字符串处理

拓展

[酱紫君的仓库](https://github.com/oovm/EulerProject)

[mma在设计上的应用](https://blog.wolfram.com/2009/02/26/exploring-logo-designs-with-mathematica/)

stackexchange[整合贴](http://mathematica.stackexchange.com/questions/18/where-can-i-find-examples-of-good-mathematica-programming-practice)



#### Jupyter的kernel配置 ####

[Linux版](https://blog.csdn.net/weixin_46584887/article/details/122760626)

Win版:

```shell
jupyter kernelspec list
```

查看当前jupyter内核列表及配置文件路径，jupyter是通过python安装的所以一般都有python的内核。

打开python的内核配置文件夹,新建与其同级的文件夹

其kernel.json文件配置如下

```json
{
	"argv":[
		"C:\\Program Files\\Wolfram Research\\Wolfram Engine\\12.2\\wolfram.exe",
		"-script",
		"C:\\Python\\lib\\WolframLanguageForJupyter\\WolframLanguageForJupyter\\Resources\\KernelForWolframLanguageForJupyter.wl",
		"{connection_file}",
		"ScriptInstall"
	],
	"display_name":"Wolfram Language 12.2",
	"language":"Wolfram Language"
}

```

wolfram.exe与KernelForWolframLanguageForJupyter.wl文件路径需要自行修改wolfram engine连接文件

连接文件下载地址：
https://github.com/WolframResearch/WolframLanguageForJupyter
