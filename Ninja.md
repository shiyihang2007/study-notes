**Ninja**是一个专注于速度的小型构建系统，由Evan Martin于2010年在[Chrome](https://zh.wikipedia.org/wiki/Google_Chrome "Google Chrome")团队工作时开发。

### 背景资料

> Evan Martin从2007年到2012年在Chrome团队工作。在加入初期，Chrome只能够在Windows上运行，他的主要任务是把代码移植到其它平台，而面临的第一个任务就是确定构建系统。
> 
> Chrome团队的成员提出了GYP增量解决方案，它的作用是从高级的描述规则生成平台相关的构建文件。
> 
> 在Linux上，他最开始尝试把[Scons](https://zh.wikipedia.org/wiki/SCons "SCons")作为GYP的目标构建系统，但当文件发生变化，启动构建就需要花费30秒时间。因为他的工作是移植代码，涉及到频繁的更改文件和重新编译，所以这被认为是不可接受的。
> 
> 后来，他又尝试[make](https://zh.wikipedia.org/wiki/Make "Make")作为GYP的目标构建系统。在刚开始的时候速度相当快，但当文件越来越多时，它变慢了。后来，他注意到make中的一些问题，觉得可以优化，因此有了开发Ninja的想法。
> 
> 在使用Ninja后，修改文件后Chrome增量构建的时间降到了6秒钟。
> 
> 使用“Ninja”命名是因为作者觉得它速度很快。
