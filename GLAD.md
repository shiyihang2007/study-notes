### 配置GLAD

GLAD是一个[开源](https://github.com/Dav1dde/glad)的库，它能解决我们上面提到的那个繁琐的问题。GLAD的配置与大多数的开源库有些许的不同，GLAD使用了一个[在线服务](http://glad.dav1d.de/)。在这里我们能够告诉GLAD需要定义的[[OpenGL]]版本，并且根据这个版本加载所有相关的[[OpenGL]]函数。

打开GLAD的[在线服务](http://glad.dav1d.de/)，将语言(Language)设置为**C/C++**，在API选项中，选择**3.3**以上的[[OpenGL]](gl)版本（我们的教程中将使用3.3版本，但更新的版本也能用）。之后将模式(Profile)设置为**Core**，并且保证选中了**生成加载器**(Generate a loader)选项。现在可以先（暂时）忽略扩展(Extensions)中的内容。都选择完之后，点击**生成**(Generate)按钮来生成库文件。

GLAD现在应该提供给你了一个zip压缩文件，包含两个头文件目录，和一个**glad.c**文件。将两个头文件目录（**glad**和**KHR**）复制到你的**include**文件夹中（或者增加一个额外的项目指向这些目录），并添加**glad.c**文件到你的工程中。

> 对于使用 [[CMake]] 的用户，你应当在 CMakeList.txt 中添加以下命令：
> ```
> target_sources(Test_1 PUBLIC glad.c)
> ```


经过前面的这些步骤之后，你就应该可以将以下的指令加到你的文件顶部了：

```c++
#include <glad/glad.h> 
```
