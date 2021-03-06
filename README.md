# jehtml - Just enough HTML

A template engine / language inspired by Visual studio code emmet abbreviations. Great for sketching.
Uses the approach of just enough similarity to html so you know all the tags, but tries to shorten as much as possible. Also tries to avoid like embraced
## Includes:
- Tab based
- advanced CSS selector
  - Symbol for ID
  - Symbol for Class
  - Symbol for types even extended to common css types
- variable insertion
- looping
- conditional rendering
- abbreviate common long attributes, tags, etc.
- almost tag independent, custom tags like components easy to integrate
- (add jquery)

## Two ways:
- While Typing as hints/suggestions or
- as a full language which gets compiled after typing.

## Lots of variation should be made possible
- explicit version (curly brackets for tag definition, semicolon as closing (old programming languages style) or every tag on new line (python-like))
- implicit version with
  - swapping symbols
  - adding symbols for own often used attributes or even tags

## Aadvantages & Disadantages

### Advantages:
- fast sketching of code snippets
- structured, forced by tabs
- Customizability
- tries to be logical (symbols, structure)

## Disadvantages:
- Readabilty suffers by using few spaces
- hard to learn
- Why do you even need this?

Just trying something crazy.
Probably abondon it as soon as my interest goes to something else. 

## Example:

```
html
	head
		meta!charset:utf-8
		title {title}
		link!rel:stylesheet!href:https://www.example.com/all.min.css
		script!defer
			$(doc).ready(() =>{

			})
		style
			body {
				text-align: center;
			}
	body#main.container!style:background-color:black;>h1>span.black test
		ul%none
			li#test$.{arr[$].author}*?{arr} {$+1}-". author: "{arr[$].author}-" | "-"I like his books.","He wrote better ones!",+
			"I get regularly disturbed by his books. But I'm fine!" 
```

- Attributes get seperated by `!` exception of ids (`#`), classes (`.`) and types (`%`)
- Attribute Names and values get sperated by `:` (or `=`)
- Variables and expressions in curly brackes `{title}`
- create direct children on the same line with `>`
- loop over elements with `*` followed by a number of iterations or the length of an array via `?{<variable_name>}`
- use `$` to get the index available in attributes, inside expression and as part of the text
- to wrap to an new line use `+` at the end of the line
- use `-` to merge expressions & strings
- in a loop use `,` to use custom strings for each iteration (has to be same amount as number of iterations)

