+++
author = "Hugo Authors"
title = "Emoji Support"
date = "2019-03-05"
description = "Hugo 表情符号使用指南"
categories = [
    "Test"
]
tags = [
    "emoji",
]
image = "the-creative-exchange-d2zvqp3fpro-unsplash.jpg"
+++

可以通过多种方式在 Hugo 项目中启用表情符号。

<!--more-->

可以直接在模板或 [内联短代码](https://gohugo.io/templates/shortcode-templates/#inline-shortcodes) 中调用 [`emojify`](https://gohugo.io/functions/emojify/) 函数。

要全局启用表情符号，请在站点的 [配置](https://gohugo.io/getting-started/configuration/) 中将 `enableEmoji` 设置为 `true`，然后您就可以直接在内容文件中输入表情符号简写代码；例如：

<p><span class="nowrap"><span class="emojify">🙈</span> <code>:see_no_evil:</code></span>  <span class="nowrap"><span class="emojify">🙉</span> <code>:hear_no_evil:</code></span>  <span class="nowrap"><span class="emojify">🙊</span> <code>:speak_no_evil:</code></span></p>
<br>

[Emoji 速记表](http://www.emoji-cheat-sheet.com/) 是表情符号简写代码的有用参考。

***

**注意** 上述步骤在 Hugo 中启用了 Unicode 标准表情符号和序列，但这些字形的渲染取决于浏览器和平台。要设置表情符号的样式，您可以使用第三方表情符号字体或字体堆栈；例如

{{< highlight html >}}
.emoji {
  font-family: Apple Color Emoji, Segoe UI Emoji, NotoColorEmoji, Segoe UI Symbol, Android Emoji, EmojiSymbols;
}
{{< /highlight >}}

{{< css.inline >}}

<style>
.emojify {
    font-family: Apple Color Emoji, Segoe UI Emoji, NotoColorEmoji, Segoe UI Symbol, Android Emoji, EmojiSymbols;
    font-size: 2rem;
    vertical-align: middle;
}
@media screen and (max-width:650px) {
  .nowrap {
    display: block;
    margin: 25px 0;
  }
}
</style>

{{< /css.inline >}}
