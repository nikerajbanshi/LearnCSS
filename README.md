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
-pixel(px),percent(%),em,rem

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
6. Transform property
7. Flexbox
8. Grid
9. Animations
10. Media Queries