<!--
# Markdown style guide
-->
# Markdown 编码风格指南

<!--
Much of what makes Markdown great is the ability to write plain text, and get
great formatted output as a result. To keep the slate clean for the next author,
your Markdown should be simple and consistent with the whole corpus wherever
possible.
-->
Markdown 强大的很大一部分原因在于它能够编写纯文本并且以优雅的格式输出。为了给下一位作者留下整洁文本，你应该尽可能的让你的 Markdown 简单并与整个文本库保持一致。

<!--
We seek to balance three goals:
-->
我们在这三个目标中寻求平衡：

<!--
1. *Source text is readable and portable.*
2. *Markdown files are maintainable over time and across teams.*
3. *The syntax is simple and easy to remember.*
-->
1. *保持源文件的可读性和可移植性。*
2. *Markdown 文件可以长期跨团队维护。*
3. *语法简单易记。*

<!--
Contents:
-->
目录：

<!--
1.  [Document layout](#document-layout)
1.  [Character line limit](#character-line-limit)
1.  [Trailing whitespace](#trailing-whitespace)
1.  [Headings](#headings)
    1.  [ATX-style headings](#atx-style-headings)
    1.  [Add spacing to headings](#add-spacing-to-headings)
1.  [Lists](#lists)
    1.  [Use lazy numbering for long lists](#use-lazy-numbering-for-long-lists)
    1.  [Nested list spacing](#nested-list-spacing)
1.  [Code](#code)
    1.  [Inline](#inline)
    1.  [Codeblocks](#codeblocks)
    1.  [Declare the language](#declare-the-language)
    1.  [Escape newlines](#escape-newlines)
    1.  [Nest codeblocks within lists](#nest-codeblocks-within-lists)
1.  [Links](#links)
    1.  [Use informative Markdown link titles](#use-informative-markdown-link-titles)
1.  [Images](#images)
1.  [Prefer lists to tables](#prefer-lists-to-tables)
1.  [Strongly prefer Markdown to HTML](#strongly-prefer-markdown-to-html)
-->
1.  [文档布局](#文档布局)
1.  [行内字符数限制](#行内字符数限制)
1.  [行尾空格](#行尾空格)
1.  [标题](#标题)
    1.  [ATX 风格的标题](#ATX-风格的标题)
    1.  [标题内插入空格](#标题内插入空格)
1.  [列表](#列表)
    1.  [对长列表使用懒惰编号](#对长列表使用懒惰编号)
    1.  [嵌套列表的缩进](#嵌套列表的缩进)
1.  [代码](#代码)
    1.  [内联代码](#内联代码)
    1.  [代码块](#代码块)
    1.  [声明代码语言](#声明代码语言)
    1.  [避免换行符](#避免换行符)
    1.  [嵌套在列表内的代码块](#嵌套在列表内的代码块)
1.  [链接](#链接)
    1.  [使用 Markdown 链接标题](#使用-Markdown-链接标题)
1.  [图片](#图片)
1.  [首选列表而非表格](#首选列表而非表格)
1.  [首选 Markdown 而非 HTML](#首选-Markdown-而非-HTML)

<!--
## Document layout
-->
## 文档布局

<!--
In general, most documents benefit from some variation of the following layout:
-->
通常来说，大多数文档都能受益于以下布局的一些变化：

```markdown
# Document Title

Short introduction.

[TOC]

## Topic

Content.

## See also

* https://link-to-more-info
```

<!--
1.  `# Document Title`: The first heading should be a level one heading, and
    should ideally be the same or nearly the same as the filename. The first
    level one heading is used as the page `<title>`.
-->
1.  `# Document Title`：第一个标题应该是一级标题，理想情况下应该与文件名几乎相同甚至完全一致。第一级标题用于页面的 `<title>` 属性。

<!--
1.  `author`: *Optional*. If you'd like to claim ownership of the document or
    if you are very proud of it, add yourself under the title. However,
    revision history generally suffices.
-->
1.  `author`：*可选*。如果你想要声明文档的所有权，或者你对它非常自豪，那把你自己添加到标题下。然而，修订历史通常就足够了。

<!--
1.  `Short introduction.` 1-3 sentences providing a high-level overview of the
    topic. Imagine yourself as a complete newbie, who landed on your "Extending
    Foo" doc and needs to know the most basic assumptions you take for granted.
    "What is Foo? Why would I extend it?"
-->
1.  `Short introduction.`：用 1-3 句话给出主题的高度概述。把自己想象成一个完全的新手，刚刚接触到你的“Foo 扩展” 文档，需要知道一些你认为理所当然的最基本假设。如，“什么是 Foo？为什么我需要扩展它？”

<!--
1.  `[TOC]`: if you use hosting that supports table of contents, such as Gitiles,
    put `[TOC]` after the short introduction. See
    [`[TOC]` documentation](https://gerrit.googlesource.com/gitiles/+/master/Documentation/markdown.md#Table-of-contents).
-->
1.  `[TOC]`：如果你使用支持目录表的托管服务，例如 Gitiles，请在简短的介绍之后加上 `[TOC]`。详情参见 [`[TOC]` documentation](https://gerrit.googlesource.com/gitiles/+/master/Documentation/markdown.md#Table-of-contents).

<!--
1.  `## Topic`: The rest of your headings should start from level 2.
-->
1.  `## Topic`：其余标题应该从二级标题开始。

<!--
1.  `## See also`: Put miscellaneous links at the bottom for the user who wants
    to know more or didn't find what she needed.
-->
1.  `## See also`：把参考链接放在底部，供想要了解更多或者未找到所需内容的用户使用。

<!--
## Character line limit
-->
## 行内字符数限制

<!--
Obey projects' character line limit wherever possible. Long URLs and tables are
the usual suspects when breaking the rule. (Headings also can't be wrapped, but
we encourage keeping them short). Otherwise, wrap your text:
-->
尽可能遵守项目的行内字符数限制。当违背规则时，通常会怀疑长链接和表格。（标题无法换行，所以我们鼓励保持短标题）此外，给你的文本分行：

```markdown
Lorem ipsum dolor sit amet, nec eius volumus patrioque cu, nec et commodo
hendrerit, id nobis saperet fuisset ius.

*   Malorum moderatius vim eu. In vix dico persecuti. Te nam saperet percipitur
    interesset. See the [foo docs](https://gerrit.googlesource.com/gitiles/+/master/Documentation/markdown.md).
```

<!--
Often, inserting a newline before a long link preserves readability while
minimizing the overflow:
-->
通常，在长链接之前插入换行符可以保持可读性，同时减少行内字符溢出：

```markdown
Lorem ipsum dolor sit amet. See the
[foo docs](https://gerrit.googlesource.com/gitiles/+/master/Documentation/markdown.md)
for details.
```

<!--
## Trailing whitespace
-->
## 行尾空格

<!--
Don't use trailing whitespace, use a trailing backslash.
-->
如果想要换行，不要使用行末空格，使用行末反斜杆。

<!--
The [CommonMark spec](http://spec.commonmark.org/0.20/#hard-line-breaks) decrees
that two spaces at the end of a line should insert a `<br />` tag. However, many
directories have a trailing whitespace presubmit check in place, and many IDEs
will clean it up anyway.
-->
根据 [CommonMark spec](http://spec.commonmark.org/0.20/#hard-line-breaks) 规定行末的两个空格应该插入 `<br />` 标记。但是，很多 directories 都有行末空格预提交检查，而且有很多 IDE 会清除行末空格。

<!--
Best practice is to avoid the need for a `<br />` altogether. Markdown creates
paragraph tags for you simply with newlines: get used to that.
-->
最好的做法是完全避免使用 `<br />`。Markdown 使用新的空行来标记段落：习惯这一点。

<!--
## Headings
-->
## 标题

<!--
### ATX-style headings
-->
### ATX 风格的标题

```markdown
## Heading 2
```

<!--
Headings with `=` or `-` underlines can be annoying to maintain and don't fit
with the rest of the heading syntax. The user has to ask: Does `---` mean H1 or
H2?
-->
带 `=` 或者 `-` 下划线的标题可能难以维护，而且不适合标题的其余语法。用户可能还会问：`---` 意味着一级标题还是二级标题呢？

```markdown
Heading - do you remember what level? DO NOT DO THIS.
---------
```

<!--
### Add spacing to headings
-->
### 标题内插入空格

<!--
Prefer spacing after `#` and newlines before and after:
-->
在 `#` 符号后面插入空格并在标题后插入空行会更好：

```markdown
...text before.

# Heading 1

Text after...
```

<!--
Lack of spacing makes it a little harder to read in source:
-->
缺乏间距使得源代码难以阅读：

```markdown
...text before.

#Heading 1
Text after... DO NOT DO THIS.
```

<!--
## Lists
-->
## 列表

<!--
### Use lazy numbering for long lists
-->
### 对长列表使用懒惰编号

<!--
Markdown is smart enough to let the resulting HTML render your numbered lists
correctly. For longer lists that may change, especially long nested lists, use
"lazy" numbering:
-->
Markdown 非常聪明，可以让生成的 HTML 正确呈现你的编号列表。对于可能更改的长列表，尤其是长的嵌套列表，请使用“懒惰”编号：

```markdown
1.  Foo.
1.  Bar.
    1.  Foofoo.
    1.  Barbar.
1.  Baz.
```

<!--
However, if the list is small and you don't anticipate changing it, prefer fully
numbered lists, because it's nicer to read in source:
-->
当然，如果列表很小而且你不希望更改它，则使用完整的编号列表更好，因为它在源代码中更可读：

```markdown
1.  Foo.
2.  Bar.
3.  Baz.
```

<!--
### Nested list spacing
-->
### 嵌套列表的缩进

<!--
When nesting lists, use a 4 space indent for both numbered and bulleted lists:
-->
当使用嵌套列表时，对编号列表和符号列表都使用 4 个空格的缩进：

```markdown
1.  2 spaces after a numbered list.
    4 space indent for wrapped text.
2.  2 spaces again.

*   3 spaces after a bullet.
    4 space indent for wrapped text.
    1.  2 spaces after a numbered list.
        8 space indent for the wrapped text of a nested list.
    2.  Looks nice, don't it?
*   3 spaces after a bullet.
```

<!--
The following works, but it's very messy:
-->
下面的代码是可用的，但是它非常混乱：

```markdown
* One space,
with no indent for wrapped text.
     1. Irregular nesting... DO NOT DO THIS.
```

<!--
Even when there's no nesting, using the 4 space indent makes layout consistent
for wrapped text:
-->
即使没有嵌套，使用 4 个空格的缩进也可以使换行的文本的布局保持一致：

```markdown
*   Foo,
    wrapped.

1.  2 spaces
    and 4 space indenting.
2.  2 spaces again.
```

<!--
However, when lists are small, not nested, and a single line, one space can
suffice for both kinds of lists:
-->
当然，当列表很小，没有嵌套，而且只有一行时，对于这两种类型的列表，一个空格就都足够了：

```markdown
* Foo
* Bar
* Baz.

1. Foo.
2. Bar.
```

<!--
## Code
-->
## 代码

<!--
### Inline
-->
### 内联代码

<!--
&#96;Backticks&#96; designate `inline code`, and will render all wrapped content
literally. Use them for short code quotations and field names:
-->
\`反引号\` 定义`内联代码`，并按照字面内容显示。它们用于短代码和字段名称中：

```markdown
You'll want to run `really_cool_script.sh arg`.

Pay attention to the `foo_bar_whammy` field in that table.
```

<!--
Use inline code when referring to file types in an abstract sense, rather than a
specific file:
-->
当引用抽象意义上的文件类型而不是特定文件时使用内联代码：

```markdown
Be sure to update your `README.md`!
```

<!--
Backticks are the most common approach for "escaping" Markdown metacharacters;
in most situations where escaping would be needed, code font just makes sense
anyway.
-->
反引号是“转义”Markdown 元字符的最常见方法；在需要转义的大多数情况下，代码字体是有意义的。

<!--
### Codeblocks
-->
### 代码块

<!--
For code quotations longer than a single line, use a codeblock:
-->
对于引用的多于一行的代码，请使用代码块：

<pre>
```python
def Foo(self, bar):
  self.bar = bar
```
</pre>

<!--
#### Declare the language
-->
#### 声明代码语言

<!--
It is best practice to explicitly declare the language, so that neither the
syntax highlighter nor the next editor must guess.
-->
最好做法是明确声明语言，以便语法高亮显示器和编辑器都不必猜测。

<!--
#### Indented codeblocks are sometimes cleaner
-->
#### 带缩进的代码块更清晰

<!--
Four-space indenting is also interpreted as a codeblock. These can look
cleaner and be easier to read in source, but there is no way to specify the
language. We encourage their use when writing many short snippets:
-->
使用四个空格进行缩进的文本也会被解释为代码块。这样的文本看起来更干净，更容易在源代码中阅读，但是无法指定语言。我们鼓励他们在编写许多简短的片段时使用它们：

```markdown
You'll need to run:

    bazel run :thing -- --foo

And then:

    bazel run :another_thing -- --bar

And again:

    bazel run :yet_again -- --baz
```

<!--
#### Escape newlines
-->
#### 避免换行符

<!--
Because most commandline snippets are intended to be copied and pasted directly
into a terminal, it's best practice to escape any newlines. Use a single
backslash at the end of the line:
-->
因为大多数命令行片段都会被复杂并直接粘贴到终端中，因此最好避免使用任何换行符。在行尾使用一个反斜杠：

<pre>
```shell
bazel run :target -- --flag --foo=longlonglonglonglongvalue \
--bar=anotherlonglonglonglonglonglonglonglonglonglongvalue
```
</pre>

<!--
#### Nest codeblocks within lists
-->
#### 嵌套在列表内的代码块

<!--
If you need a codeblock within a list, make sure to indent it so as to not break
the list:
-->
如果你需要在列表中放置一个代码块，请保证缩进它，以免破坏列表：

```markdown
*   Bullet.

    ```c++
    int foo;
    ```

*   Next bullet.
```

<!--
You can also create a nested code block with 4 spaces. Simply indent 4
additional spaces from the list indentation:
-->
你也可以用 4 个空格的缩进创建一个嵌套的代码块。只需要在列表缩进上额外缩进 4 个空格。

```markdown
*   Bullet.

        int foo;

*   Next bullet.
```

<!--
## Links
-->
## 链接

<!--
Long links make source Markdown difficult to read and break the 80 character
wrapping. **Wherever possible, shorten your links**.
-->
长链接会使 Markdown 源文本难以阅读并打破 80 个字符换行限制。所以无论如何，尽可能缩短你的链接。

<!--
### Use informative Markdown link titles
-->
### 使用 Markdown 链接标题

<!--
Markdown link syntax allows you to set a link title, just as HTML does. Use it
wisely.
-->
Markdown 链接语法允许你设置链接标题，就像在 HTML 里的做法一样。明智地使用它。

<!--
Titling your links as "link" or "here" tells the reader precisely nothing when
quickly scanning your doc and is a waste of space:
-->
如果把链接的标题标为“链接”或者“这里”，当读者快速浏览你的文档时，这并不能告诉他们任何东西，这是在浪费空间：

```markdown
See the syntax guide for more info: [link](syntax_guide.md).
Or, check out the style guide [here](style_guide.md).
DO NOT DO THIS.
```

<!--
Instead, write the sentence naturally, then go back and wrap the most
appropriate phrase with the link:
-->
相反，自然地写作，然后回过头来，把最合适的短语标记成为链接：

```markdown
See the [syntax guide](syntax_guide.md) for more info.
Or, check out the [style guide](style_guide.md).
```

<!--
## Images
-->
## 图片

<!--
Use images sparingly, and prefer simple screenshots. This guide is designed
around the idea that plain text gets users down to the business of communication
faster with less reader distraction and author procrastination. However, it's
sometimes very helpful to show what you mean.
-->
少用图片，尽量用简单的截图。本指南的设计理念是，纯文本可以避免分散读者的注意力及作者的拖沓，让用户更快地进行交流。当然，有时图片也有助于展示你的想法。

<!--
See [image syntax](https://gerrit.googlesource.com/gitiles/+/master/Documentation/markdown.md#Images).
-->
参见 Markdown [图片语法](https://gerrit.googlesource.com/gitiles/+/master/Documentation/markdown.md#Images)。

<!--
## Prefer lists to tables
-->
## 首选列表而非表格

<!--
Any tables in your Markdown should be small. Complex, large tables are difficult
to read in source and most importantly, **a pain to modify later**.
-->
你的 Markdown 中任何表格都应该很小。复杂、大型的表格很难在源代码中阅读，更重要的是**后续难以维护**。

```markdown
Fruit | Attribute | Notes
--- | --- | --- | ---
Apple | [Juicy](https://example.com/SomeReallyReallyReallyReallyReallyReallyReallyReallyLongQuery), Firm, Sweet | Apples keep doctors away.
Banana | [Convenient](https://example.com/SomeDifferentReallyReallyReallyReallyReallyReallyReallyReallyLongQuery), Soft, Sweet | Contrary to popular belief, most apes prefer mangoes.

DO NOT DO THIS
```

<!--
[Lists](#lists) and subheadings usually suffice to present the same information
in a slightly less compact, though much more edit-friendly way:
-->
[列表](#列表) 和子标题通常足以以不那么紧凑的方式展示同样的内容，但更便于编辑：

```markdown
## Fruits

### Apple

* [Juicy](https://SomeReallyReallyReallyReallyReallyReallyReallyReallyReallyReallyReallyReallyReallyReallyReallyReallyLongURL)
* Firm
* Sweet

Apples keep doctors away.

### Banana

* [Convenient](https://example.com/SomeDifferentReallyReallyReallyReallyReallyReallyReallyReallyLongQuery)
* Soft
* Sweet

Contrary to popular belief, most apes prefer mangoes.
```

<!--
However, there are times when a small table is called for:
-->
当然，有时候也需要一个小表格：

```markdown
Transport | Favored by | Advantages
--- | --- | ---
Swallow | Coconuts | Otherwise unladen
Bicycle | Miss Gulch | Weatherproof
X-34 landspeeder | Whiny farmboys | Cheap since the X-38 came out
```

<!--
## Strongly prefer Markdown to HTML
-->
## 首选 Markdown 而非 HTML

<!--
Please prefer standard Markdown syntax wherever possible and avoid HTML hacks.
If you can't seem to accomplish what you want, reconsider whether you really
need it. Except for [big tables](#prefer-lists-to-tables), Markdown meets almost
all needs already.
-->
请尽可能地使用标准 Markdown 语法并避免夹杂 HTML。如果你觉得不能实现你想要的特性，那重新考虑你是否真的需要它。除了 [大表格](#首选列表而非表格)，Markdown 已经几乎满足了所有需求。

<!--
Every bit of HTML or Javascript hacking reduces the readability and portability.
This in turn limits the usefulness of integrations with
other tools, which may either present the source as plain text or render it. See
[Philosophy](philosophy.md).
-->
每一处插入的 HTML 或者 Javascript 代码都会降低可读性和可移植性。这反过来又限制了同其他工具的集成，这些工具可以以纯文本或者预览的方式呈现源文件。参见[哲学](philosophy.md)。

<!--
Gitiles does not render HTML.
-->
Gitiles 不支持 HTML。