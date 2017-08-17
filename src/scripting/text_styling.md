Text Scripting
==============

## tput
Allows to color some text very easily

### Example
```bash
echo "$(tput setaf 1)Hello world" # prints red "Hello world"
echo "$(tput bold)Hello$(tput sgr0) world" # prints bold "Hello"
```
### Output
> <font color="#FF0000">Hello world</font><br>
> <strong>Hello</strong> world

### Text style commands
```bash
tput setaf N  # Select foreground color
tput setab N  # Select background color
tput bold     # Select bold mode
tput dim      # Select dim (half-bright) mode
tput smul     # Enable underline mode
tput rmul     # Disable underline mode
tput rev      # Turn on reverse video mode
tput smso     # Enter standout (bold) mode
tput rmso     # Exit standout mode
tput sgr0     # Reset text format to the terminal's default
```

### Cursor move commands
```bash
tput cup Y X # Move cursor to screen postion X,Y (top left is 0,0)
tput cuf N   # Move N characters forward (right)
tput cub N   # Move N characters back (left)
tput cuu N   # Move N lines up
tput ll      # Move to last line, first column (if no cup)
tput sc      # Save the cursor position
tput rc      # Restore the cursor position
tput lines   # Output the number of lines of the terminal
tput cols    # Output the number of columns of the terminal
```

### Editing commands
```bash
tput ech N   # Erase N characters
tput clear   # Clear screen and move the cursor to 0,0
tput el 1    # Clear to beginning of line
tput el      # Clear to end of line
tput ed      # Clear to end of screen
tput ich N   # Insert N characters (moves rest of line forward!)
tput il N    # Insert N lines
```