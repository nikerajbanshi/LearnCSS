## CSS(Cascading Style Sheet)
-syntax: selector{property:value;}
*Linking CSS 
1.Inline style
2.Internal style
3.External style
*Selectors in CSS
---->Universal selector(*),element selector(p,h1-h6,etc..)
---->class selector(.), id selector(#)
*Priority of selectors
-(id>class>element)
*Units in CSS
1. fixed units
-pixel(px)
2. relative units
percent(%),em,rem
-em:
-->used to set up font size and width
-->font size of the parent
eg:if the parent div has font-size:10px, and the child div is set to 2em then it will have (10*2 px) of font-size
-rem:
-->font-size of the root element

**Remember this**
1. CSS Cascading Property
--> it is a cascade algorith which tells what property will apply to the element
--> if the elements have same selectors, the property which comes later will apply to that element
2. CSS Specificity Property
--> is a calculated value assigned to the selectors(tells the priority of the selectors)
---> inline style>id>class i.e inline style has more specificity
## CSS Properties
1. Color Property
-color systems--> Named, RGB(0-255), Hex code(0-9,A-F)
-background-color
-alpha in rgb: eg: rgba(0,255,255,0.5)--->alpha(a) values ranges from 0 to 1 (0 means hidden)
-opacity:applies effect on all elements--->same function as alpha(0-1)
2. Text property
-text align:right,left,center,justify
-text decoration:none,line-through,underline,overline
-text-transform:uppercase,lowercase,capitalize
-line-height:1.5, letter-spacing:2px
-font weight(0-900), font-size:20px, font-family:sans-serif , font-style:italic,bold,....
3. Box-Model property
-height/width(in px)
-border/border-radius
-margin
-padding
4. Display property
-display:inline --->sets elements in one horizontal line
-display:block ---->sets elements in next line one by one 
-display:inline-block ---->keeps the original height and width and displays in inline way
5. Position property
-position: static, relative, absolute, fixed , sticky
-position static: default value : doesn't respond to position offsets
-position relative: sets position relative to itself
-position absolute: 1. sets position according to the whole document (if no parent positioned element)
                    2. Positioned relative to the nearest positioned ancestor (i.e., the nearest parent with position: relative | absolute | fixed | sticky)
                    3. takes no space
-position fixed: The element is fixed relative to the viewport — even if you scroll, it stays in the same position.
                 Often used for navbars, floating buttons, etc

-position sticky: Acts like relative until you scroll past a threshold,then it “sticks” like fixed.
                  Depends on top, bottom, left, or right offsets.

7. Flexbox
display: flex; → activates Flexbox

Main vs Cross Axis:
  - row → main: horizontal | cross: vertical
  - column → main: vertical | cross: horizontal

justify-content (main axis):
  - flex-start | flex-end | center | space-between | space-around | space-evenly

align-items (cross axis):
  - flex-start | flex-end | center

flex-wrap:
  - wrap | nowrap | wrap-reverse

align-content:
  - used only when flex-wrap is applied
  - flex-start | flex-end | center | space-between | space-around

align-self:
  - overrides align-items for a single item

gap:
  - adds space between flex items

flex-grow / flex-shrink / flex-basis:
  - controls how items grow, shrink, or set initial size

 eg:
 .container {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  align-items: center;
  gap: 20px;
}


8. Grid


display: grid; → activates Grid layout

Grid System:
  - Two-dimensional layout system (controls both rows & columns)
  - Used for creating full page or section layouts

Grid Structure:
  - Rows → horizontal lines
  - Columns → vertical lines
  - Each box formed is a grid cell

grid-template-columns / grid-template-rows:
  - Defines number & size of columns or rows
  - Example:
    grid-template-columns: 200px 1fr 2fr;
    grid-template-rows: 100px auto;

repeat():
  - Creates repeating columns/rows easily
  - Example: grid-template-columns: repeat(3, 1fr);

fr unit:
  - Represents a fraction of available space
  - Example: 1fr 2fr → 1 part and 2 parts width respectively

gap:
  - Adds space between grid rows and columns
  - Example: gap: 20px;

grid-column / grid-row:
  - Defines where an item starts and ends
  - Example:
    grid-column: 1 / 3;  /* spans column 1 to 3 */
    grid-row: 1 / 2;

grid-area:
  - Shorthand → row-start / column-start / row-end / column-end
  - Example:
    grid-area: 1 / 1 / 2 / 3;

justify-items (horizontal alignment of items):
  - start | end | center | stretch

align-items (vertical alignment of items):
  - start | end | center | stretch

justify-content (horizontal alignment of entire grid):
  - start | end | center | space-between | space-around

align-content (vertical alignment of entire grid):
  - start | end | center | space-between | space-around

9. Transform Property
-rotate(in deg)--> rotates along defined degree
-scale(in value)---> increases or decreases size
-skew(in deg) ---> bends at certain angle 
-translate(in px)---->moves a plane

10. Transition property
-means changing from one state to another
-transition shorthand
    property name | duration |  timing-function | delay;

    eg: transition: margin-right , 1s, linear, 0.5s;

11. Animations
-To animate css elements
-animation: animation-name |animation-duration |animation-timing-function |animation-delay| animation-iteration-count| animation-direction
-Syntax(@keyframes animation_name {from {property:value} to {property:value}})
or (@keyframes animation_name{0%{property:value},20%{property:value}.......100%{property:value}})

12. Media queries
-To make responsive design
-syntax: @media(min-width:200px){ h1{property:value}}

--------------------------------------------------
13. other CSS property

i.  BOX Shadow property
--> box-shadow:x-offset | y-offset | blur | color;

ii. background-image
-->background-image:url(./path/file_name);
-->background-size:contain,cover,auto;

iii. Pseudo class
-->is a keyword added to the selector to specify the state of the selected elements
1.hover
2.active
3.checked
4.nth-of-type

 Syntax--> h1:hover{property:value}
     
iv. Pseudo element
--> is a keyword added to the selector used to  specify the specific part of the element
Syntax--> h1::first-letter{property:value}

v. Z-index
--> decides the stack level of elements
**Remember this**
--> the more the Z-index of the element, the more the element will appear at the top
--> should specify the position of the element first to appply z-index property
-->z-index works with all position except static position
--> if +ve value (z-index) appears at the top and if -ve (z-index) appears at the bottom

eg: z-index:1 , -2 