# Python Notes

## Quick Links

[Chapter 1-7](#chapter-1-7)  
[Chapter 8](#chapter-8)  
[Chapter 9](#chapter-9)  
[Chapter 10](#chapter-10)

## Some Explanations

These are backups of my notes while reading a python tutorial book.

[How to Think Like a Computer Scientist: Learning with Python 3 (RLE)](http://openbookproject.net/thinkcs/python/english3e/)  
[Source Repo of the book](https://code.launchpad.net/~thinkcspy-rle-team/thinkcspy/thinkcspy3-rle)

I don't know if it's a good book or not, but it's better than nothing anyways. And I feel pretty good up to now.

Notes are only for myself. If there is something I already know, I won't write it down.

> PS: By reading a book on a computer, I think PDF is for the hard-copy books, and HTML is for computers. It's way better to read a webpage rather than a pdf document. I don't know if we can read HTML offline on iPads, or highlight texts, make notes while reading HTML on iPads/PC. Auto adopt size and adjustable font size, just these two features completely beats PDF. It should be like "scrolling through a page" rather than "turning pages of a book". Right, nowadays there are formats for ebooks. Textbooks may should be published along with a html-like format?? That might be too expensive tho.

## Notes

<a id="chapter-1-7"></a>
### Chapter 1-7

- `type()`
    prints var's type. ex:`<class 'str'>`
    
- Math Operations
    - `+` `-` `*` 
    - `/`  returns float
    - `//` returns int, rounding to the left
    - `**` for power
    - `%` for modulus

- Convert between types, use `int(), float(), str(),` etc.
    
- Get input from user, use `n = input("Prompt")`

- For-loop: `for i in range(x):`

- `asset()`

- docstrings
    ```python
    def function_one():
        """ Prints something. """ # This is docstring
        print("...")
    ```
    It will appear as help information in autocomplete.

- in Python, functions **always return values**, if none is specified, `None` is returned.

- Boolean operators: `!= == <= >= < >` `and` `or` `not`

- Conditionals:
    ```python
    if x < y:
        STATEMENTS
    elif x > y:
        STATEMENTS
    else:
        STATEMENTS
    ```
- Naming
    > I am not used to these
    - Use CamelCase for classes
    - lowercase_with_underscores for functions and variables
    
- Get Caller's Line Number: `import sys` `line_num = sys._getframe(1).f_lineno`
    
- format string: `str = "I have {0} apples.".format(num)`

- while statement:
    ```python
    while True:
        ...
    ```
    
- `break` `continue`

- Paired Data
    ```python
    person = ("Alex", 1998)
    people = [("...", 1999), ("...", 2000), ... ]
    for (name, year) in people:
        if year > 2000:
            ...
    ```


### 8. Strings <a id="chapter-8"/>

- string usages: 
    ```python
    str = "string"
    str[0], str[3:5], str[3:], str[:5], str[-1]
    ```

- Strings are immutable: 
    `greeting[0] = "J"   # ERROR`

- `in` and `not in` operators

    ```python
    "p"     in "apple"   # True
    ""      in "apple"   # True
    "apple" in "apple"   # True
    ```

- `find` and `split`
    split omits any white space

- Punctuation
    `import string; if letter in string.punctuation`

- format specification
    `"{0:…}".format(varA)`
    - Use `<` `^` `>` along with a number for aligments
        ex. {0:<10}
    - Use `f` for float, `x` for hexadecimal
    - Use `.2f` for float with 2 decimals


### 9. Tuples <a id="chapter-9"/>

- Tuples are immutable
- To create a single element tuple, add a comma in the end. ex: a = (5,)
- Use tuples to swap varibles. ex: (a, b) = (b, a)


### 10. Event-Driven Programming <a id="chapter-10"/>

- Keypress events
    ```python
    import turtle

    # To listen for a key, simply:
    def h1():
        tess.forward(30)

    wn.onkey(h1, "Up")

    wn.listen()
    wn.mainloop()
    ```

    - To refer to a key: use "q", "Cancel", "Up", "Down", etc. (10.1)

- keyword `global`:
    ```python
    a = 10
    def f():
        global a
        print(a)

    f()   # Will print 10
    ```
- Mouse events:
    - Mouse events on the window
        ```python
        def h1(x, y):
        tess.goto(x, y)
        wn.onclick(h1)  # Wire up a click on the window.
        wn.mainloop()
        ```

    - Mouse events on the turtle
        ```python
        def handler_for_tess(x, y):
            tess.forward(30)

        def handler_for_alex(x, y):
            alex.forward(50)

        tess.onclick(handler_for_tess)
        alex.onclick(handler_for_alex)

        wn.mainloop()
        ```
    > Ok, where is `self`? How to generalize this?
    
    - Timer 
        ```python
        def h1():
            tess.forward(100)
            tess.left(56)

        wn.ontimer(h1, 2000)
        ```
        - the timer is automatically released once fired. Therefore, we need to do this:
        ```python
        def h1():
            tess.forward(100)
            tess.left(56)
            wn.ontimer(h1, 60)

        h1()
        ```

    