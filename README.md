# node-ansi

ANSI CSI library for node.js

---

## CSI API
	
This library contains the necessary methods to use ANSI positioning and coloring
in a node.js application. 
	
### Properties
	
	/* foreground colors */
	fg:
		black, red, green, yellow, blue, magenta, cyan,
		lightgray, darkgray, lightred, lightgreen, lightyellow,
		lightblue, lightmagenta, lightcyan, white
	
	/* background colors */
	bg:
		black, red, green, yellow, blue, magenta, cyan, white
	
	/* "normal" attributes */	
	normal
	
	/* attribute (writes to stdout) getter/setter */
	attributes

### Methods

	gotoxy(x,y)        // go to screen position x,y
	getxy()            // return current screen position (broken)
	pushxy(name,x,y)   // store current position (no arguments)
	                   // or save x,y under the given name
	popxy(name)        // restore saved position (no arguments)
	                   // or restore x,y from given name
	up(n)              // move cursor up n spaces
	down(n)            // move cursor down n spaces
	left(n)            // move cursor left n spaces
	right(n)           // move cursor right n spaces
	ins(n)             // insert n spaces
	del(n)             // delete n spaces
	clear()            // clear the screen
	cleartoeol()       // clear to the end of the line
	home()             // goto x=1, y=1
	write(str)         // output a string to stdout
	strlen(str)        // return the length of a string minus ANSI codes

