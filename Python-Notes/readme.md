# Python Notes

These are backups of my notes while reading a python tutorial book.

[How to Think Like a Computer Scientist: Learning with Python 3 (RLE)](http://openbookproject.net/thinkcs/python/english3e/)

[Source Repo of the book](https://code.launchpad.net/~thinkcspy-rle-team/thinkcspy/thinkcspy3-rle)

I don't know if it's a good book or not, but it's better than nothing anyways. And I feel pretty good up to now.

Notes are only for myself. If there is something I already know, I won't write it down.

> PS: By reading a book on a computer, I think PDF is for the hard-copy books, and HTML is for computers. It's way better to read a webpage rather than a pdf document. I don't know if we can read HTML offline on iPads, or highlight texts, make notes while reading HTML on iPads/PC. Auto adopt size and adjustable font size, just these two features completely beats PDF. It should be like "scrolling through a page" rather than "turning pages of a book". Right, nowadays there are formats for ebooks. Textbooks may should be published along with a html-like format?? That might be too expensive tho.

## Notes

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
    ```
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
    ```
    while True:
        ...
    ```
    
- `break` `continue`

- Paired Data
    ```
    person = ("Alex", 1998)
    people = [("...", 1999), ("...", 2000), ... ]
    for (name, year) in people:
        if year > 2000:
            ...
    ```
    
    

