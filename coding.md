# Coding

## Indentation and Alignment

Very few coding style guides that I have read have made any distinction between
indentation and alignment, and even the few that did, it was only a very brief
mention. However, I believe that these two things are very different and need
to be considered separately.

Summary:

* Exactly 1 (one) tab MUST be used per level of indentation.
* Spaces MUST be used for alignment.

### Indentation

Indentation is a whitespace representation of the nesting level of code. The
following example illustrates multiple levels of indentation:

```
for i in 1..100:
	if is_even(i):
		print 'Even!';
	end
end
```

Each level of nesting must be indented exactly one level, and each level of
indentation must use exactly one tab. There are a number of benefits to using tabs over spaces for indentation, but among them are the following:

* Tabs have a configurable visual width
* Tabs have a smaller bytesize
* Tabs take a smaller number of keystrokes with no editor configuration

### Alignment

Unlike indentation, which represents the logical or lexical nesting level in
code, alignment is purely aesthetic. It is used to make code more readable by
ligning up variable assignments, logical conditions, etc. Spaces must be used for alignment, as in the following example:

```
some_var       = 1
some_other_var = 2
```

### Combining Indentation & Alignment

All of the arguments which I have heard against using tabs for indentation
confuse the concepts of indentation and alignment. A common complaint is that
when using tabs, if a different tab width is used, then the code "looks ugly."
When indentation and alignment are properly differentated, however, this
immediately becomes a nonissue. As tabs are used only for indentation, and
spaces for alignment, code retains its proper alignment even upon tab resize. For example, combining our two previous examples:

```
for i in 1..100:
	if is_even(i):
		some_var       = 1
		some_other_var = 2	
		print 'Even!';
	end
end
```

One should note that even when the tabs used for indentation are resized, the code maintains its proper alignment. Tabs must never be used for alignment.
