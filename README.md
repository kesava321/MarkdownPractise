Roses are red  
Violets are blue

Sugar is sweet


perform_complicated_task

do_this_and_do_that_and_another_thing


* https://www.google.com
* https://google.com/
* ftp://ftp.us.debian.org/debian/
* smb://foo/bar/baz
* irc://irc.freenode.net/gitlab
* http://localhost:3000


>>>
If you paste a message from somewhere else

that

spans

multiple lines,

you can quote that without having to manually prepend `>` to every line!
>>>


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

With inline diffs tags you can display  {additions}  or  [deletions] .

The wrapping tags can be either curly braces or square brackets  {additions}  or  [deletions] .

However the wrapping tags cannot be mixed as such:


{+ additions +]
[+ additions +}
{- deletions -]
[- deletions -}