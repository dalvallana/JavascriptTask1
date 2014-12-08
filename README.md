Specifications
==============

- The above pseudo-constant values may vary. However, it is guaranteed that:

	a) containerWidth >= (nRectangles x maxRectDim)
		and
	b) containerHeight >= (nRectangles x maxRectDim)

	so that the "on load" processing below is always possible.

- The action takes place in a (containerWidth x containerHeight) container random-color div with top-left corder at 0,0 screen (window) coordinates.

- On load, nRectangles random-sized (each side minRectDim to maxRectDim pixels included) and random-color rectangles are displayed according to the following rules:

	a) They must not overlap eachother
	b) They must be fully contained within the container div
	c) Their position is random, given the above two constraints

	The mouse cursor position at load is ignored.

- Each time a mouse cursor is positioned over a rectangle, it must change color to a new random color.

- If the cursor remains over a rectangle for 3 seconds, the rectangle is re-positioned (no animation) in such a way that:

	a) It is no longer under the mouse cursor position
	b) It is still fully visible within the container div
	c) It does not overlap with the other rectangles

		Should these be impossible, the rectangle is permanently removed

	d) The new position is random, given the above three constraints


Further notes
-------------
- You may use a framework, yet raw DOM would be appreciated.
- Focus on clean and readable/understandable code before focusing on performance.
- Once done, we will ask to expose /viva voice/ the way you have proceeded to write the program.