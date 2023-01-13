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
say`map act box thirteen past three`
each box got put into a point list with the label "act". Move cursor to the "sprint" button: `point act nine`.

#### Finding more boxes
- `upper` box size upper bound.
- `lower` box size lower bound.
- `threshold` the filtering threshold. The higher the number, the lighter that colors can be distinguished.
- `flex info` toggles a view of the current grid 
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
select the wrong row, `row <letter>` move to 1 B C.

#### More modes
- `grid phonetic`
- `grid frame` switches to frame mode

#### Grid size
- `grid bigger`
- `grid smaller`
 `bump`, e.g. `grid bigger bump`.

The default size `flex_mouse_settings.talon` - change the number in `user.flex_mouse_grid_field_size = "30"`.

#### Grid visibility
- `background lighter`
- `background darker`
- `letters lighter`
- `letters darker`