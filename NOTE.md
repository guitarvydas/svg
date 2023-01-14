DaS {
  ...
  ContainedRectangle = Rectangle Rectangle @isSmaller(B,A) @isInside(B,A)
  
  SmallerRect<RectB,RectA> = Rect<RectA> Rect<RectB> @smaller(RectB, RectA)
  Inside<RectB,RectA> = Rect<RectA> Rect<RectB> xy(...) @inside(RectB, RectA)
  ...
}
