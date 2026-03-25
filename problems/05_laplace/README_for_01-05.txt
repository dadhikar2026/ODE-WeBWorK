
WeBWorK PG Bundle: Linear Systems Solved by Laplace Transforms
==============================================================

Files included
--------------
1. laplace_system_01_basic_coupled.pg
2. laplace_system_02_forced_constant.pg
3. laplace_system_03_triangular.pg
4. laplace_system_04_impulse_piecewise.pg
5. laplace_system_05_harmonic_system.pg

Design goals
------------
- Complete standalone PG files
- Randomized coefficients chosen from safe parameter sets
- Explicit answer-checking syntax using Formula(...)->cmp()
- Instructor comments embedded in each file
- Solution outlines embedded in each file
- Style aligned with a first ODE course (MATH 2306 level)

Implementation notes
--------------------
- These problems avoid random choices that create awkward repeated-root or singular cases.
- The impulse problem checks two equivalent formulas:
      sin(w*(t-a))/w * step function
  but to maximize portability, the answer blank asks for the equivalent
      piecewise-style shifted expression with Heaviside notation omitted:
      (sin(w*(t-a))/w) * (t>=a)
  Since many WeBWorK installations do not parse Boolean expressions well,
  this version instead asks only for the formula valid for t>a and states
  the full solution in the solution section. If your server has a Heaviside
  macro, you can upgrade the checker.

Student syntax reminders
------------------------
Use:
  exp(3*t), sin(2*t), cos(2*t)

not:
  e^(3t), sin 2t, cos 2t

Common macros used
------------------
PGstandard.pl
MathObjects.pl
answerHints.pl
parserFormulaUpToConstant.pl   (only included when convenient; not required)

Instructor customization
------------------------
- You can edit variable ranges in the randomization section of each file.
- You can add scaffolding answer blanks for Laplace-domain work:
      X(s), Y(s)
  if you want a multi-part version.
- You can convert any file into a scaffolded problem by replacing one
  answer blank with several intermediate answer blanks.

