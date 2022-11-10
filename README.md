# kisp-rs
☯ KOONLISP interpreter written in Rust

## Koonlisp (kisp)

A lisp like language that is serializable to JSON only using arrays of numbers.

### Example 1: Math

We want to add the numbers 2 and 2.

In a classic language, this might look like:

``` javascript
add(2, 2)
```

We can translate that to a lisp like language:

``` common-lisp
(add 2 2)
```

In that example we assume the add function's name is `add`, but in KISP we can only use numbers, so we will change it to `1` (1 is arbatrary and can be any number). This would look like this:

``` common-lisp
(1 2 2)
```

All we need to do is turn this list into valid JSON by changing the paranthesis and adding commas.

``` json
[1, 2, 2]
```

### Example 2: ASCII Strings

We want to have the string: `"hello"`

Looking at an ASCII table we can get all the ascii codes.

| Character | Code |
|-----------|------|
| h         | 104  |
| e         | 101  |
| l         | 108  |
| l         | 108  |
| o         | 111  |

We can use an ASCII string function (lets say `16` for example), and insert all the ascii codes.

``` json
[16, 104, 101, 108, 108, 111]
```


