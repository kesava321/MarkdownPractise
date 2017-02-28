#Markdown Practice
###Newline
Roses are red  
Violets are blue

Sugar is sweet

### Multiple Underscore In Words

perform_complicated_task

do_this_and_do_that_and_another_thing

### URL Auto-Linking

* https://www.google.com
* https://google.com/
* ftp://ftp.us.debian.org/debian/
* smb://foo/bar/baz
* irc://irc.freenode.net/gitlab
* http://localhost:3000

### Multiline Blockquote
>>>
If you paste a message from somewhere else

that

spans

multiple lines,

you can quote that without having to manually prepend `>` to every line!
>>>

### Code and Syntax Highlighting
Inline `code` has `back-ticks around` it.

```javascript
var s = "JavaScript syntax highlighting";
alert(s);
```

```python
def function():
    #indenting works just fine in the fenced code block
    s = "Python syntax highlighting"
    print s
```

```ruby
require 'redcarpet'
markdown = Redcarpet.new("Hello World!")
puts markdown.to_html
```

```
No language indicated, so no syntax highlighting.
s = "There is no highlighting for this."
But let's throw in a <b>tag</b>.
```


### Inline Diff

```diff
+With inline diffs tags you can display  {"additions"}  or  ["deletions"] .
-Test removal
```

The wrapping tags can be either curly braces or square brackets  [+ additions +]  or  [- deletions -] .


However the wrapping tags cannot be mixed as such:

{+ additions +]
[+ additions +}
{- deletions -]
[- deletions -}


### Emoji
Sometimes you want to :monkey: around a bit and add some :star2: to your :speech_balloon:. Well we have a gift for you:

:zap: You can use emoji anywhere GFM is supported. :v:

You can use it to point out a :bug: or warn about :speak_no_evil: patches. And if someone improves your really :snail: code, send them some :birthday:. People will :heart: you for that.

If you are new to this, don't be :fearful:. You can easily join the emoji :family:. All you need to do is to look up on the supported codes.

Consult the [Emoji Cheat Sheet](http://emoji.codes) for a list of all supported emoji codes. :thumbsup:


### Special GitLab References

GFM recognizes special references.

You can easily reference e.g. an issue, a commit, a team member or even the whole team within a project.

GFM will turn that reference into a link so you can navigate between them easily.

GFM will recognize the following:
Refer to https://gitlab.com/gitlab-org/gitlab-ce/blob/master/doc/user/markdown.md 

| input                      | references                      |
|:---------------------------|:--------------------------------|
| `@user_name`               | specific user                   |
| `@group_name`              | specific group                  |
| `@all`                     | entire team                     |
| `#123`                     | issue                           |
| `!123`                     | merge request                   |
| `$123`                     | snippet                         |
| `~123`                     | label by ID                     |
| `~bug`                     | one-word label by name          |
| `~"feature request"`       | multi-word label by name        |
| `%123`                     | milestone by ID                 |
| `%v1.23`                   | one-word milestone by name      |
| `%"release candidate"`     | multi-word milestone by name    |
| `9ba12248`                 | specific commit                 |
| `9ba12248...b19a04f5`      | commit range comparison         |
| `[README](doc/README)`     | repository file references      |
| `[README](doc/README#L13)` | repository file line references |

GFM also recognizes certain cross-project references:

| input                                   | references              |
|:----------------------------------------|:------------------------|
| `namespace/project#123`                 | issue                   |
| `namespace/project!123`                 | merge request           |
| `namespace/project%123`                 | milestone               |
| `namespace/project$123`                 | snippet                 |
| `namespace/project@9ba12248`            | specific commit         |
| `namespace/project@9ba12248...b19a04f5` | commit range comparison |
| `namespace/project~"Some label"`        | issues with given label |

It also has a shorthand version to reference other projects from the same namespace:

| input                         | references              |
|:------------------------------|:------------------------|
| `project#123`                 | issue                   |
| `project!123`                 | merge request           |
| `project%123`                 | milestone               |
| `project$123`                 | snippet                 |
| `project@9ba12248`            | specific commit         |
| `project@9ba12248...b19a04f5` | commit range comparison |
| `project~"Some label"`        | issues with given label |

### Task Lists


You can add task lists to issues, merge requests and comments. To create a task list, add a specially-formatted Markdown list, like so:

```no-highlight
- [x] Completed task
- [ ] Incomplete task
    - [ ] Sub-task 1
    - [x] Sub-task 2
    - [ ] Sub-task 3
```

- [x] Completed task
- [ ] Incomplete task
    - [ ] Sub-task 1
    - [x] Sub-task 2
    - [ ] Sub-task 3

Tasks formatted as ordered lists are supported as well:

```no-highlight
1. [x] Completed task
1. [ ] Incomplete task
    1. [ ] Sub-task 1
    1. [x] Sub-task 2
```

1. [x] Completed task
1. [ ] Incomplete task
    1. [ ] Sub-task 1
    1. [x] Sub-task 2

Task lists can only be created in descriptions, not in titles. Task item state can be managed by editing the description's Markdown or by toggling the rendered check boxes.


### Videos

Image tags with a video extension are automatically converted to a video player.

The valid video extensions are `.mp4`, `.m4v`, `.mov`, `.webm`, and `.ogv`.

    Here's a sample video:

    ![Sample Video](img/markdown_video.mp4)

Here's a sample video:

![Sample Video](img/markdown_video.mp4)

### Math

It is possible to have math written with the LaTeX syntax rendered using [KaTeX][katex].

Math written inside ```$``$``` will be rendered inline with the text.

Math written inside triple back quotes, with the language declared as `math`, will be rendered on a separate line.

Example:

    This math is inline $`a^2+b^2=c^2`$.

    This is on a separate line
    ```math
    a^2+b^2=c^2
    ```

Becomes:

This math is inline $`a^2+b^2=c^2`$.

This is on a separate line
```math
a^2+b^2=c^2
```

_Be advised that KaTeX only supports a [subset][katex-subset] of LaTeX._

>**Note:**
This also works for the asciidoctor `:stem: latexmath`. For details see the [asciidoctor user manual][asciidoctor-manual].