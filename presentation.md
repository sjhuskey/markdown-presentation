---
title: "Using Markdown"
author: "Samuel J. Huskey"
date: "2024-12-03"
---

## What is Markdown?

Markdown is (awkwardly) a markup language that's easy to use and remarkably versatile. If you're tired of bloated applications like Microsoft Word that keep introducing new ways to get in the way of your writing, Markdown might be the solution for you!

## Why you should use Markdown

- Simple syntax
- Separates writing from layout
- Cross-platform compatibility
- Easily tracked with version control systems like Git
- Long-term viability
- One input, many outputs—including web sites!

## What do you need to use Markdown?

- A text editor (e.g., TextEdit, Notepad++, VS Code, etc.)
- … that's it! :smiley:

## How do you use Markdown?

### Headings

- \# First level heading
- \## Second level heading
- \### Third level heading
- Can you guess what the fourth level heading looks like? :thinking:

### Paragraphs

Just start writing. Keep writing until you want to start a new paragraph. At that point, stop writing and press the return key twice.

Now, start a new paragraph and keep writing.

Easy!

### Typography

If you want to put something in italics, surround it with one asterisk on each side, *like this*.

Do you want bold type? Use *two* asterisks instead of one on each side, **like this**.

Markdown does not have a defined syntax for underlining. But that's okay, since underlining was originally the way to signal to typesetters that something should be in italics or boldface type! If you *really* need to underline something, you can use `<u>` and `</u>`, `<u>`like this`</u>` (but you won't see any underlining here   :frowning:).

You *can* do strikethrough text by surrounding text with two ~ characters on each side, ~~like this~~.

To use superscript, surround the character with ^ characters, ^like^ ^this^.

Subscript is similar, but you use the ~ character, ~like~ ~this~.

### Lists

If you want to make a bullet list:

- First bullet  
- Second Bullet
- Third Bullet

If you want to make a numbered list:

1. First item
2. Second item
3. Third item

OR: Let your Markdown interpreter keep track of items for you!

1. First item
1. Second item
1. Third item

If you need a nested list, simply indent the nested part:

- First item
- Second item
  - First subitem
  - Second subitem
- Third item

1. First item
1. Second item
    1. First subitem
    1. Second subitem
1. Third item

### Blockquotes

Blockquotes are super easy: you just put a > in front of the paragraph.

> Here's a blockquote
>
> Here's another blockquote

This is a regular paragraph. :smiley:

### Hyperlinks

There are two types of hyperlinks in Markdown. There's a hyperlinked URL and hyperlinked text.

To hyperlink a URL, simply surround it with < and >: <https://www.markdownguide.org/>.

To hyperlink some text, enclose the text in [ and ] and then put the hyperlink next to it in ( and ): [Markdown Guide](https://www.markdownguide.org/).

### Code blocks

To include code in a sentence, use the "tick" character, `like this`. This way, you can talk about `for` loops in Python, for example.

You can also include full blocks of code by opening and closing them with three ticks. You should also include the name of the computer language right after the opening ticks:

```python
import pandas as pd

df = pd.read_csv('my-csv-file.csv')
```

```html
<p>Here's some HTML text. Writing in HTML requires a lot more effort than Markdown does.</p>

<p>For example, here's an ordered list:</p>

<ol>
    <li>First item</li>
    <li>Second item</li>
</ol>
```

Bonus! Here's a horizontal rule:

***

## Advanced Markdown

### Footnotes

There are two ways of inserting footnotes.[^1]

[^1]: This is the first way.

Another way of inserting footnotes is to include everything in line.^[Like this. Now everything I write in this space will appear in a footnote. Also, most Markdown interpreters will automatically number these notes.] Here, I'll show you what I mean.^[This note should be number 3. :smiley:]

### Tables

I don't recommend trying to make tables manually in Markdown. It can be done, but it's much easier to use a tool like [Donat Studios' Free CSV to Markdown Table Generator](https://donatstudios.com/CsvToMarkdownTable).

But just so that you can see what a Markdown table looks like:

| First Column | Second Column | Third Column |
|--------------|---------------|--------------|
| Item 1       | Another Item  | A third item |
| 1000         | 2000          | 3000         |

### Images

You need to know where the image is located on your computer to insert it into a Markdown document. If you know that bit of information, the rest is easy:

![A caption for an image of a cow!](./Cow_horned_portrait.jpg "Alt text for an image of a cow.")

## Pandoc

Pandoc is a command line tool that will convert a Markdown document into almost any other format you might be expected to produce. It's incredibly simple to use, too.

You just open a Terminal window and enter

```bash
pandoc -s yourfilename.md -o yourfilename.[file-extension]
```

For example, to turn this document into a Microsoft Word document (`.docx`), I'd do this:

```bash
pandoc -s presentation.md -o presentation.docx
```

To turn it into a LaTeX document.

```bash
pandoc -s presentation.md -o presentation.latex
```

You should definitely check out Pandoc. It's like a Swiss Army Knife for document formats!

## Static Web Site Generators

Many static web site generators like [Eleventy](https://www.11ty.dev/) (Yay!) and [Jekyll](https://jekyllrb.com/) (Boo!) use Markdown for basic content.

## Publishing Platforms

I just heard about [Quarto](https://quarto.org/), "an open-source scientific and technical publishing system"

## Markdown Resources

### Guides

- [Markdown Guide](https://www.markdownguide.org/)
- [Pandoc's Markdown](https://pandoc.org/MANUAL.html#pandocs-markdown)
- [Markdown for VS Code](https://code.visualstudio.com/Docs/languages/markdown)
- [Markdown Emoji Cheat Sheet](https://github.com/ikatyang/emoji-cheat-sheet)

### Tools

#### Stand-alone Editors

- [VS Code](https://code.visualstudio.com/), with Markdown extensions
- [Ghost](https://ghostwriter.kde.org/)

#### Online Editors

- [StackEdit Online Markdown Editor](https://stackedit.io/)
- [Dillinger Online Markdown Editor](https://dillinger.io/)

#### Other

- [Pandoc](https://pandoc.org/MANUAL.html): Convert Markdown to a variety of other file formats
- [CSV to Markdown Table Generator](https://donatstudios.com/CsvToMarkdownTable)
