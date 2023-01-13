# Flex Mouse Grid

- `map <word>` creates a new point at the current location of the mouse cursor with the label "word"
- `unmap <word>` deletes the point labeled "word"
- `unmap everything` deletes all points for the active window. Careful with this one!
- `points` shows all points for the current window
- `points close` hides all points
- `grid close` hides all points, all boxes, and the dense grid
- `point <word>` moves to the point labeled "word"
- `point click <word>` clicks the point labeled "word"
- `point righty <word>` right clicks the point labeled "word"
- `point <word> three`
- `boxes` finds boxes labeling each with a number.
- `box <number>` moves the cursor to the specified box, hiding the boxes afterwards
- `box click <number>` clicks the specified box, hiding the boxes afterwards
- `box righty <number>` right clicks the specified box, hiding the boxes afterwards
- `boxes close` hides all boxes
- `grid close` hides all boxes, all points, and the dense grid
- `map <word> box <number>` creates a new point at the center of the chosen box labeled "word"
- `map <word> box <number1> mark <number2>...` creates a point list of two points. You can include more points by including more `mark <number>`s.
- `map <word> box <number1> past <number2>` creates a point list that will include a point for every box in the range between "box number1" and "box number2". 
say `map sprint box five` to create a point there:
move to the "sprint" button with the phrase `point sprint`
We could say`map act box thirteen past three` which would create a point list as seen below:
each box got put into a point list with the label "act". Move cursor to the same "sprint" button with the following: `point act nine`.

### Finding more boxes
- `upper` box size upper bound. Boxes will not be larger than this number of pixels.
- `lower` box size lower bound. Boxes will not be smaller than this number of pixels.
- `threshold` the filtering threshold. The higher the number, the lighter that colors can be distinguished.
- `flex info` toggles a view of the current grid and box configuration parameters
modify these parameters
- `boxes <parameter> more`
- `boxes <parameter> less`

So e.g. `boxes upper more` would increase size 
- `boxes <parameter> more bump`
- `boxes <parameter> less bump`
- `boxes threshold`

to toggle an overlay of the processed image.
- `flex grid` to show the grid. 
- `flex grid screen`  whole screen
- `flex grid screen <number>` different screen
- `grid close` 

### Changing your mind

If you have selected the wrong number, you can choose a different number anytime. If you have selected the wrong row, you can say `row <letter>`, 
will result in moving the cursor to coordinate 1 B C.

### More modes

If frame mode does not suit you, there are two other modes that can be used to show the coordinates.

- `grid checker` turns on checker mode, which overlays the coordiantes in a checker pattern. This can be visually confusing, but it splits the difference between being able to immediately see the coordinate and being able to see the contents of your screen.
- `grid full` shows every possible coordinate.
- `grid phonetic` switch to phonetic mode, which is just like frame mode except with full phonetic words labeling the rows and columns instead of individual letters.
- `grid frame` switches to frame mode (the default).

### Grid size

- `grid bigger`
- `grid smaller`

You can adjust the size by a smaller amount by including `bump`, e.g. `grid bigger bump`.

The default size of the grid can be set in `flex_mouse_settings.talon` by changing the number in `user.flex_mouse_grid_field_size = "30"`.

### Grid visibility

The grid can be made more or less transparent with the following commands.

- `background lighter`
- `background darker`
- `letters lighter`
- `letters darker`

You can also include the word `bump` to adjust the value by a smaller amount. For instance, `background darker bump`.

### Grid color

Every color in the grid is modifiable in flex_mouse_settings.talon, allowing you to set the defaults to whatever is comfortable.

The colors use 6 digit hexadecimal RGB colors.
The transparency uses 2-digit hexadecimal numbers for an alpha channel.

## To do

- Implement "next point", "last point" for point lists
- Configurable characters: alphabet, alphabet subset, numeric
- Deduplicate grid config state
- Allow clearing saved grid config, box config
- Include more things in grid config
- Automatic threshold detection?
