Lab Project 0: ASCII Printing
===================================
# Description
This demo code builds a program "asciidraw" that prints ASCII art.

# Anticipated learing outcomes
This playful assignment is primarily intended to enable students to achieve and demonstrate competencies 
related to 
- Use of program command-line driver development tools including an edtior, c compiler, make, and git.
- Concepts described in chapters 1-4 of Kernigham & Ritchie's "C Programming Language" such as
  - Declaration & definition of functions and various integer types.
  - Control flow, including goto.
  - Bitwise operators such as shift (<<) and AND (&).
  - Separate compilation and the role of include/header files.

By engaging students in the analysis and modification of algorithms that render ASCII art, 
this project will also introduce concepts related to raster graphics including

- The projection of simple planar geometric shapes into a discrete raster plane.
- The use of bitmaps to encode rasterized patterns.

# Files

The following are source files for asciidraw
- uimain.c: Main file with the UI to interact with the user. Given the user input, it prints the desired shape.
- draw_shapes.c: Defines functions to draw simple shapes (e.g. square, triangle)
- draw_chars.c: Defines functions to draw characters.
- 11x16font.c: Defines bitmap array of 11x16 font (11 rows, 16 cols).  Each col is stored as a bitmap of type short
- draw.h: Header file containing all the declarations of the relevant methods used in this demo.

You can compile this program using the command

    $ cc  -g -O3 -o asciidraw uimain.c draw_shapes.c draw_chars.c 11x16font.c
 
- This command is a nuisance to type.  
- The TAs will show you how the program *make* can more conveniently and efficiently compile asciidraw.
- Efficiency: due to only compiling those .c files whose source has been changed more recently than their .o files.
- Convenience: due to make reading a database called Makefile specifying dependencies among files.

The following command runs the program

    $ ./asciidraw

The following files are provided for your convenience (but not presently used)
- 5x7font.c: defines the bitmaps of a 5x7 font (5 rows, 7 cols).  Each col is stored as a bitmap of type char
- 8x12font.c: defines the bitmaps of an 8x12 font (8 rows, 12 cols).  Each row is stored as a bitmap of type char.

# Pleae try to be polite and respectful
  Java's coding styles are subtly different from C's.
  These styles developed for both pragmatic and idiosyncratic reasons.
  It's rude (and unprofessional) to ignore others' cultural norms.  
  Generosity and sensitivity are universally appreciated.

Please observe the following standard C coding practices:
- Multiple related functions are defined in the same source file (e.g. draw_shapes.c).  
  Otherwise a project would contain an overwhelming number of files.
- Type definitions are collected in just a few (in this case one) include file (draw.h).
  Please read it.
- Giant function and variable definitions (e.g. the font bitmap arrays) are stored in their own files. 
  Otherwise the files containing them would be overwhelmingly long.
- C's indention is (slightly) different than Java.  Feel free to ask about the differences.  
  Some of it is pragmatically motivated, some is just idiosyncratic.
- Traditionally, C uses underscores_to_separate_words and to denote constants in ALL_CAPS.  
  CamelCase is now also acceptable.  Please try to be consistent.
- Similar coding practices are employed when writing assembly language.

# Instructions

- The TAs will lead you through the process of adding a function to
  print arrows. This will require you to (1) define function
  print_arrow() in print_shapes.c, (2) Adding a declaration for
  print_arrow() to draw.h, and (3) add a command "t" to uimain.c.

- You will independently add another font to this project.  
  You are welcome to use either the 5x7 or 8x12 fonts we provide.  
  To reference the font file, you'll also need to modify the Makefile.
  
  # Learning outcomes
  
  - ability to use emacs editor and linux command-line compilation tools using bash shell
  - git: ability to clone repo and add/commit/push changes 
  - ability to understand and modify C programs with separate compilation and include files 
  - bitfield manipulation
  - able to use make & understand and modify Makefiles 
  - abile to understand and modify simple programs written in C

