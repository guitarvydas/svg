This is a trivial (very trivial) example of parsing an SVG rectangle.

The SVG is:
```
<svg version="1.1" width="300" height="300" xmlns="http://www.w3.org/2000/svg">
  <rect fill="gray" stroke="black"/>
</svg>
```

The parser is written in Ohm-JS:
```
SVG {
  Blueprint =  "<svg" stuff ">" GraphicObject+ "</svg>"
  GraphicObject =
    | Rect
  Rect = "<rect" stuff "/>"
  stuff = (~">" ~"/>" any)+
}
```

and a screenshot of the parse, in Ohm-Editor, is:
~[trivial SVG parser](parser.png)

The SVG looks like this in a browser:
~[rect](rect.png)

It is easy to extend the grammar to include more details, like x,y,width,height,fill,stroke, etc., etc.
