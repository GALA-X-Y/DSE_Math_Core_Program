# DSE Math Core Program
This repository contains mathematics programs on Casio Fx Series (HKEAA Approved), tested in HKDSE 2024.

## Notes Before Using
### Entering Programs
- If you don't know how to input the special keys like `Lbl`, `IfEnd`, you may refer to [special_key.md](https://github.com/GALA-X-Y/DSE_Math_Core_Program/blob/main/special_key.md)
- Keys in blue are single. For example, [³√(]() is single key, but not the combination of  ³ and √(.

### After Entering Programs
- Check the total bytes of the program, recheck your program if there is a difference.
- **!!!Test your program with some sample cases!!!**, you may ask ChatGPT to generate some.

### Type of Programs
These are tags that indicates the properties of the programs.
- **Result-Return**: The program will return the result of the calculations into variable cells. (reuse the answer in other programs)
- **Input-Preserve**: The program will not change the input variable cells. (reuse the same input in other programs)

Without these two tags, the program will change the input variable cells and will not return the result to variable cells.

## How to Use
Click [Program 1](https://github.com/GALA-X-Y/DSE_Math_Core_Program/blob/main/DSE_CoreProgram/P1.md), [Program 2](https://github.com/GALA-X-Y/DSE_Math_Core_Program/blob/main/DSE_CoreProgram/P2.md), [Program 3](https://github.com/GALA-X-Y/DSE_Math_Core_Program/blob/main/DSE_CoreProgram/P3.md), [Program 4](https://github.com/GALA-X-Y/DSE_Math_Core_Program/blob/main/DSE_CoreProgram/P4.md) to get source code of following programs.

### Program 1 - Linear Equations
Variable Cells Used: All
Bytes: 220
Modes: 4
```
Input D (modes) #1, 2, 3, 4

When D=1, solve simultaneous equations
Input A, B, C, M, X, Y which {Ax+By=C...(1), Mx+Xy=Y...(2)
Output x and y of the intercept point

When D=2, find distance, slope, and equation of straight line from two points
(Input-Preserve & Result-Return)
Input A, B, X, Y which Point 1:(A, B), Point 2:(X, Y)
Output distance from Point 1 to Point 2
Output slope of straight line pass through Point 1 and Point 2, return this to M
Output a, b, c which ax+by+c=0 (straight line pass through Point 1 and Point 2)*
*For some cases, a, b and c are multiplied by a same factor, you have to manually divide it.

When D=3, find y-intercept from one point and a slope
(Input-Preserve & Result-Return)
Input A, B, M which Point 1:(A, B), Slope: M
Output y-intercept, return this to C

When D=4, find middle point and perpendicular slope of two points
(Result-Return)
Input A, B, X, Y which Point 1:(A, B), Point 2:(X, Y)
Output x and y of middle point, return x to A, y to B
Output slope of perpendicular bisector, return to M
```

### Program 2 - Expand Functions and Cosine Formula
Variable Cells Used: All
Bytes: 161
Modes: 3
```
Input D (modes) #1, 2, 3

When D=1, expand functions
(Input-Preserve)
Input A, B, C, M, X, Y which (Ax²+Bx+C)(Xx²+Yx+M)
Output a, b, c, d, e which ax⁴+bx³+cx²+dx+e (expand above functions)

When D=2, find the angle with three sides using cosine formula
(Input-Preserve)
Input A, B, C which are the sides of triangle
Output the angle opposite to A, adjacent to B and C

When D=3, find another side adjacent to the angle using cosine formula
(Input-Preserve)
Input A, B, C which A is opposite side, B is the adjacent side, C is the angle
Output another adjacent side to the angle
```

### Program 3 - Solve Cubic Equation
Variable Cells Used: A, B, C, D, X
Bytes: 136
Modes: 1
Condition: Must be under Deg mode (SHIFT→MODE→1)
```
Input A, B, C, D which Ax³+Bx²+Cx+D=0
Output root 1, root 2, root 3 (Math Error when no real roots)
```

### Program 4 - Circle
Variable Cells Used: All
Bytes: 129
Modes: 2
Condition: Must be under Deg mode (SHIFT→MODE→1)
```
Input D (modes) #1, 2

When D=1, find centre and radius
Input A, B, C which x²+y²+Ax+By+C=0
Output x and y of centre
Output Radius

When D=2, find the intersect points with a straight line
Input A, B, C which x²+y²+Ax+By+C=0
Input X, Y, M which Xx+Yy=M
Output x and y of first intercept point
Output x and y of second intercept point
```

## License

This program is released under the GNU General Public License v3.0.

Project Developed by Hugo Law.

For more details, see the [LICENSE](https://github.com/GALA-X-Y/DSE_Math_Core_Program/blob/main/LICENSE.txt) file or visit [GNU General Public License v3.0](https://www.gnu.org/licenses/gpl-3.0.en.html).
