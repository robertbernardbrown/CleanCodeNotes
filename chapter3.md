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
### One Level of Abstraction per Function
* Abstraction level should be carefully followed
  * high level abstractions like `getHTML()` shouldn't be mixed with lower level abstractions like `.append('\n')`
  * can keep readers from understanding core concepts to the function
### Reading Code From Top to Bottom: The Stepdown Rule
* Code to read like a top-down narrative
  * should read as a set of 'To' paragraphs
  > TO include the setups and teardowns, we include setups, then we include the test pafe content, and then we include the teardowns
  > To include the setups, we include the suite setup if this is a suire, then we include the regular setup, etc
  * This technique can help programmers keep functions abstracted to one level
### Switch Statements
* Hard to make small switch statements
* They will always do N amount of things
  * Best we can do is bury switches in low level classes and keep them DRY
  * Put switches in an abstract factory that will use the switch case only once
### User Descriptive Names
* The smaller and more focused a function is, the easier it is to write a descriptive name
* A Long, descriptive name is better than a short, enigmatic name
  * Don't be afraid of long names
  * Try reading the code a few times with different names in place
* Be consistent in your names
  * I.E. you name s function `includeTeardownPages`, then name others: `includeSuiteTeardownPages`, `includeSetupPage`, etc