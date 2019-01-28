# Chapter 3 of Clean Code - Functions

## Functions should be small
* Limited lines - hardly ever be longer than 20 lines long
* The smaller the better and more understandable
### Blocks and Indenting
* Within conditional statements, the blocks should only be one line long
  * Keeps things long and documentary
* Indent level of a function should not be longer than one or two
  * Easier to read and understand
### Do One Thing
* Functions should do one thing. They should do it well. They should do it only.
  * If a function does only those steps that are one level below the stated name of the function, then the function is only doing one thing
  * Example:  

  > TO RenderPageWithSetupsAndTeardowns, we check to see whether the page is a test page and if so, we include the setups and teardowns. In either case we render the page in HTML.  
  
* can you extract another function from your function with a name that is not a restatement of the implementation?