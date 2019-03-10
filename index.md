<!-- Google Style Guides -->
Google 编码风格指南
===================

<!-- Every major open-source project has its own style guide: a set of conventions
(sometimes arbitrary) about how to write code for that project. It is much
easier to understand a large codebase when all the code in it is in a
consistent style. -->
每个大型的开源项目都有自己的编码风格指南：关于如何为该项目编写代码的一组约定（有时是任意的）。当一个大型代码库中的所有代码都是一致的样式时，它的可读性就更高了。

<!-- “Style” covers a lot of ground, from “use camelCase for variable names” to
“never use global variables” to “never use exceptions.” This project
([google/styleguide](https://github.com/google/styleguide)) links to the
style guidelines we use for Google code. If you are modifying a project that
originated at Google, you may be pointed to this page to see the style guides
that apply to that project. -->
“样式”涵盖了很多方面，从“使用驼峰式命名法”到“不使用全局变量”到“不使用异常”。这个项目（[google/styleguide](https://github.com/google/styleguide)）我们在编写 Google 代码时使用的风格指南。如果你在修改 Google 发起的项目，那你可能会被引导到本页以阅读应用于该项目的编码风格指南。

<!-- This project holds the [C++ Style Guide][cpp], [Objective-C Style Guide][objc],
[Java Style Guide][java], [Python Style Guide][py], [R Style Guide][r],
[Shell Style Guide][sh], [HTML/CSS Style Guide][htmlcss],
[JavaScript Style Guide][js], [AngularJS Style Guide][angular],
[Common Lisp Style Guide][cl], and [Vimscript Style Guide][vim]. This project
also contains [cpplint][cpplint], a tool to assist with style guide compliance,
and [google-c-style.el][emacs], an Emacs settings file for Google style. -->
本项目包含[C++ 编码风格指南][cpp]、[Objective-C 编码风格指南][objc]、[Java 编码风格指南][java]、[Python 编码风格指南][py]、[R 编码风格指南][r]、[Shell 编码风格指南][sh]、[HTML/CSS 编码风格指南][htmlcss]、[JavaScript 编码风格指南][js]、[AngularJS 编码风格指南][angular]、[Common Lisp 编码风格指南][cl] 以及 [Vimscript 编码风格指南][vim]。本项目还包含 [cpplint][cpplint]，一个编码风格检查工具，和 [google-c-style.el][emacs]，一份 Google 编码风格的 Emacs 配置文件。

<!-- If your project requires that you create a new XML document format, the [XML
Document Format Style Guide][xml] may be helpful. In addition to actual style
rules, it also contains advice on designing your own vs. adapting an existing
format, on XML instance document formatting, and on elements vs. attributes. -->
如果你的项目要求你创建一份新的 XML 文档格式，那么 [XML Document Format Style Guide][xml] 可能有所帮助。除了已有的样式规则以外，在章节 XML 实例文档格式化以及元素与属性中，它还包含有关自行设计或修改现有格式的建议。

<!-- The style guides in this project are licensed under the CC-By 3.0 License,
which encourages you to share these documents.
See [https://creativecommons.org/licenses/by/3.0/][ccl] for more details. -->
本项目中的编码风格指南受 CC-By 3.0 许可保护，该许可鼓励你共享这些文档。详细信息请查阅 [https://creativecommons.org/licenses/by/3.0/][ccl]。

<!-- The following Google style guides live outside of this project:
[Go Code Review Comments][go] and [Effective Dart][dart]. -->
以下 Google 编码风格指南位于本项目之外：[Go 代码审查注解][go]和[高效的 Dart][dart].

<a rel="license" href="https://creativecommons.org/licenses/by/3.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by/3.0/88x31.png" /></a>

[cpp]: ./cppguide.html
[objc]: ./objcguide.md
[java]: ./javaguide.html
[py]: ./pyguide.html
[r]: ./Rguide.xml
[sh]: ./shell.xml
[htmlcss]: ./htmlcssguide.html
[js]: ./jsguide.html
[angular]: ./angularjs-google-style.html
[cl]: ./lispguide.xml
[vim]: ./vimscriptguide.xml
[cpplint]: https://github.com/google/styleguide/tree/gh-pages/cpplint
[emacs]: https://raw.githubusercontent.com/google/styleguide/gh-pages/google-c-style.el
[xml]: ./xmlstyle.html
[go]: https://golang.org/wiki/CodeReviewComments
[dart]: https://www.dartlang.org/guides/language/effective-dart
[ccl]: https://creativecommons.org/licenses/by/3.0/
