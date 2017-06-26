For clarity, let the "hexagonal" coordinates be `(r,g,b)` where `r`, `g`, and `b` are the **red**, **green**, and **blue** coordinates, respectively.  The coordinates `(r,g,b)` and `(x,y)` are related by the following:

    y = 3/2 * s * b
    b = 2/3 * y / s
    x = sqrt(3) * s * ( b/2 + r)
    x = - sqrt(3) * s * ( b/2 + g )
    r = (sqrt(3)/3 * x - y/3 ) / s
    g = -(sqrt(3)/3 * x + y/3 ) / s

    r + b + g = 0

**Derivation:**

 - I first noticed that any horizontal row of hexagons (which should have a constant `y`-coordinate) had a constant `b` coordinate, so `y` depended only on `b`.  Each hexagon can be broken into six equilateral triangles with sides of length `s`; the centers of the hexagons in one row are one and a half side-lengths above/below the centers in the next row (or, perhaps easier to see, the centers in one row are 3 side lengths above/below the centers two rows away), so for each change of `1` in `b`, `y` changes `3/2 * s`, giving the first formula.  Solving for `b` in terms of `y` gives the second formula.

 - The hexagons with a given `r` coordinate all have centers on a line perpendicular to the r axis at the point on the `r` axis that is `3/2 * s` from the origin (similar to the above derivation of `y` in terms of `b`).  The `r` axis has slope `-sqrt(3)/3`, so a line perpendicular to it has slope `sqrt(3)`; the point on the `r` axis and on the line has coordinates `(3sqrt(3)/4 * s * r, -3/4 * s * r)`; so an equation in `x` and `y` for the line containing the centers of the hexagons with `r`-coordinate `r` is `y + 3/4 * s * r = sqrt(3) * (x - 3sqrt(3)/4 * s * r)`.  Substituting for `y` using the first formula and solving for `x` gives the second formula. (This is not how I actually derived this one, but my derivation was graphical with lots of trial and error and this algebraic method is more concise.)

 - The set of hexagons with a given `r` coordinate is the horizontal reflection of the set of hexagons with that g coordinate, so whatever the formula is for the `x` coordinate in terms of `r` and `b`, the `x` coordinate for that formula with `g` in place of `r` will be the opposite. This gives the third formula.

 - The fourth and fifth formulas come from substituting the second formula for `b` and solving for `r` or `g` in terms of `x` and `y`.

 - The final formula came from observation, verified by algebra with the earlier formulas.
