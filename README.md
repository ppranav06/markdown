# Markdown
A quick reference to markdown

---


You should read this, it's **very important**. (bold)
You _might_ want to read this. (italic)
~~Never mind~~ - it wasn't _that_ important. (strikethrough)

Let's try a few `combinations`: 
**This text is strong, ~~this text is strong with strikethrough~~, and _this text is formatted with strong emphasis_**
***This text is formatted with strong emphasis too.***


# Heading 1
## Heading 2
### Heading 3
#### Heading 4
##### Heading 5
###### Heading 6


The underscores on the next line create a thematic break below this paragraph.
___
The minus signs below must be separated from this paragraph by a blank line.
If not, they are parsed as a level 2 heading.

----
Three or more asterisks also create a thematic break.
****


> Use quote blocks to emulate reply text.
> This line is part of the same quote.

This line is not formatted and does not belong to the quote block.

> This block spans multiple paragraphs.
>
> The second paragraph is grouped with the previous paragraph in the same quote block.
> Character formatting is _also_ supported inside the **quote block**.

> Quote blocks can also be nested.
>> When you start a new line with additional > characters,
>>> it simulates a threaded conversation.


Start an indented code block following a paragraph with a blank line and at least four spaces of indentation:

    This is a code block.

    Blank lines between indented lines do not end the code block.

    Here is some HTML:
        <div class="footer">
            © 2009—2017 JetBrains · All rights reserved
        </div>
This line of text is not indented. It ends the code block and starts a new paragraph.


Set multiple lines of code in fenced code blocks.

```
action: function(ctx) {
    workflow.check(!ctx.issue.isChanged('votes'), workflow.i18n('Voting for a resolved issue is not allowed.'));
},
```

The following code block uses syntax highlighting for Haskell:
```hs
-- Point-free style
fib :: Integer -> Integer
fib = (fibs !!)
where fibs = 0 : scanl (+) 1 fibs

-- Explicit
fib :: Integer -> Integer
fib n = fibs !! n
where fibs = 0 : scanl (+) 1 fibs
```

(Lists) Things I need to do today:
1. Fix usability problem
2. Clean up the page
   * Make the headings bigger
2. Push my changes
3. Create code review
   * Describe my changes
   * Assign reviewers
     * Ask for feedback


Kitchen Cleanup Rotation

| Month    | Assignee | Backup |
| -------- | -------- | ------ |
| January  | Dave     | Steve  |
| February | Gregg    | Karen  |
| March    | Diane    | Jorge  |

Here's the same text with character formatting.
+ The text in the first column is flush right.
+ The text in the second column is centered.
+ The Markdown is stripped down to the minimum syntax that is required to render the table.

Month | Assignee | Backup
---:|:---:| ---
**January** | Dave | _Steve_
**February** | Gregg | _Karen_
**March** | Diane | _Jorge_


[inline link](https://www.jetbrains.com)
[inline link with tooltip](https://www.jetbrains.com "JetBrains: Development Tools for Professionals and Teams")
[reference link][1]

[1]: https://www.jetbrains.com


Here's an image link to the Markdown logo on Wikipedia:

Inline:
![Markdown logo](https://upload.wikimedia.org/wikipedia/commons/thumb/4/48/Markdown-mark.svg/208px-Markdown-mark.svg.png "Markdown")

Reference style:
![Markdown logo][logo]

[logo]: https://upload.wikimedia.org/wikipedia/commons/thumb/4/48/Markdown-mark.svg/208px-Markdown-mark.svg.png "Markdown"

Markdown also supports images as links.
Just wrap the entire image reference in brackets then add the target URL in parenthesis after the image reference.
People use this syntax to insert a thumbnail image that links to a video on a video sharing platform.

Here's a reference to the latest video promotion for YouTrack:

[![YouTrack — Maintain Order In A World of Chaos](https://img.youtube.com/vi/rhAunB7UQFQ/sddefault.jpg)](https://www.youtube.com/watch?v=rhAunB7UQFQ)


Here are a few examples of backslash escapes:

\*not emphasis*
\`not an inline code span`
1\. not an ordered list
\* not an unordered list
\# not a heading

\This is not a backslash escape - the escaped character is not a markup character.
