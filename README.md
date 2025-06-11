# comp1100-assignment-1-solved
**TO GET THIS SOLUTION VISIT:** [COMP1100 Assignment 1 Solved](https://mantutor.com/product/comp1100-solved/)


---

**For Custom/Order Solutions:** **Email:** mantutorcodes@gmail.com  

*We deliver quick, professional, and affordable assignment help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;97770&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;3&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;5&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;5\/5 - (3 votes)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;COMP1100 Assignment 1 Solved&quot;,&quot;width&quot;:&quot;138&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 138px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            5/5 - (3 votes)    </div>
    </div>
In this assignment, you will build a Haskell program that uses the CodeWorld API to draw colourful shapes on the screen.

{:.msg-info} This assignment is worth 10% of your final grade.

Required Knowledge

If you have finished the Week 3 lab, you should be able to complete Part A.

If you have finished the Week 4 lab, you should be able to complete the majority of the assignment. Some parts require recursion over lists, which is covered in the Week 5 lab.

Overview of Tasks

COMP1100 Marks

Task 1: Helper Functions 20 marks

Task 2: Rendering Shapes 35 Marks Task 3: Handling Events 30 Marks

Technical Report 15 marks Total 100 marks

Getting Started

1. Fork the assignment repository and create a project for it in VSCodium, following the same steps as in Lab 2. The assignment repository is at https://gitlab.cecs.anu.edu.au/comp1100/2022s2/2022s2StudentFiles/Assignment1.

2. Add our version of the repository as a remote called upstream. This allows us to provide additional fixes in the unlikely case that they are required. You do this by doing the following:

3. Go to the command palette in VSCode (or VSCodium) by pressing Ctrl + Shift + p

4. Type git remote

5. Click Git: Add Remote

6. Enter upstream into the box for the remote name 7. Put the following URL as the remote url: https://gitlab.cecs.anu.edu.au/comp1100/2022s2/2022s2StudentFiles/Assignment1.git.

Overview of the Repository

Most of your code will be written to Haskell files in the src/ directory. We are using the model-view-controller pattern to structure this assignment. Each file is called a module, and we use modules to group related code together and separate unrelated code.

Model.hs

The model is a data type that describes the state of the running program. The program will move to new states (new values of type Model) in response to user actions, as defined by the controller.

View.hs

The view turns the model into something that can be shown on the screen; in this project, that is the CodeWorld Picture type.

Controller.hs

The controller considers user input (and other events), along with the current model, and uses that to decide what the new model should be.

Other Files

tests/ShapesTest.hs contains some unit tests – simple checks that verify small parts of your program are working correctly. You are not required to write tests for this assignment, but you might find it useful to do so. tests/Testing.hs is a small testing library used by tests/ShapesTest.hs. You are not required to understand it for this assignment. app/Main.hs ties your functions together into the final program that runs. You are not required to understand it.

comp1100-assignment1.cabal tells the cabal build tool how to build your assignment. You are not required to understand this file, and we will discuss how to use cabal below.

Setup.hs tells cabal that this is a normal package with no unusual build steps. Some complex packages (that we won’t see in this course) need to put more complex code here. You are not required to understand it.

Overview of Cabal

cabal is the build tool for Haskell programs and libraries. It provides several useful commands:

cabal v2-run shapes: Build your assignment (if necessary), and run the shapes program. Note that you will need to enter Ctrl-C in your terminal to exit the program.

cabal v2-repl comp1100-assignment1: Run the GHCi interpreter over your project. This gives you the same ghci environment you use in labs, but with the assignment code loaded. (Aside: REPL is the name for interactive sessions like GHCi – it stands for read-eval-print loop. Many modern languages have REPLs.) cabal v2-test: Build and run the tests. Tests will abort on the first failure, or the first call to a function that is still undefined.

{:.msg-info} You should execute these cabal commands in the top-level directory of your project, e.g.

~/comp1100/assignments/Assignment1 (i.e., the directory you are in when you launch the VSCodium Terminal for your project).

Overview of the Program

You use a web browser to interact with the shapes program that you launched with cabal v2-run shapes. Once you have completed the assignment, it will respond to the following actions:

| Action | Effect | |—————————-|————————————————————-| | Esc (key) | Clear the canvas | | S

(key) | Display a sample image | | C (key) | Change colour (of shape to draw) | | T (key) | Change tool (type of shape to draw) | |

Task 1: Helper Functions (20 marks)

The easiest way to solve a large problem is often to break it apart into smaller, easier problems. Programming is the same. In this task you will write some helper functions that will make future tasks easier. You can test your implementations by running cabal v2-test.

The functions you need to write for this task are:

toolToLabel in src/View.hs. This function should return instructions for the user on how to use each Tool, according to the following table:

| Tool | Label | |——————–|————————————————————————-| | LineTool | “Line: clickdrag-release” | | PolygonTool | “Polygon: click at least three times, then spacebar” | | RectangleTool | “Rectangle: click-drag release between opposite corners” | | CircleTool | “Circle: click-drag-release between opposite points on the circumference”| | TriangleTool | “Triangle: click-drag release along the hypotenuse” | | EllipseTool | “Ellipse: click-drag-release along the major axis” |

Note: At the time this assignment is released, the course will have only briefly covered lists. You do not need to manipulate lists to write toolToLabel; you can use a blank pattern (_) to ignore them.

nextColour in src/Controller.hs. This function should return the next colour in our set of ColourNames:

| Argument | Result | |———-|———-| | Black | Pink | | Pink | Red | | Red | Orange | | Orange | Brown | | Brown | Green | | Green | Blue | |

Blue | White | | White | Black |

nextTool in src/Controller.hs. This function implements tool-switching, but should not change Tool if the user is halfway through an operation:

If the tool is not holding a point (that is, a non-PolygonTool tool holding Nothing (in all applicable fields) or a PolygonTool holding the empty list []), select the next tool in the following sequence: Line -&gt; Polygon -&gt; Rectangle -&gt; Circle -&gt; Triangle -&gt; Ellipse -&gt; Line. Note that you will have to initialise the Double value of the EllipseTool to a suitable value.

If there is a Point stored in the given tool (because it is holding a Just value or the list in PolygonTool is non-empty), return the argument unchanged.

If this is unclear, study the nextToolTests in test/ShapesTest.hs.

Note: At the time this assignment is released, the course will have only briefly covered lists. You can write the PolygonTool case for nextTool without using list recursion. Use [] to match an empty list. In a subsequent case, give the entire list a name like points to match any nonempty list (or find a way to use the _ pattern!).

Part A ends here.

Submitting Part A

Your submission for Part A should include implementations of toolToLabel, nextColour, and nextTool that compile without warnings (except where the warnings are concerned with Part B code), and pass the tests run by cabal v2-test. You are welcome to continue working on Part B of your assignment and committing and pushing changes, so long as your code continues to compile without errors and the tests continue to pass.

Part B begins…

Task 2: Rendering Shapes (35 marks)

In src/View.hs, modelToPicture converts your Model type into a CodeWorld Picture, so that it can be displayed on the screen. It currently does not work, because colourShapesToPicture is undefined. In this task you will fill in that missing piece, building up a function to convert the [ColourShape] from your Model into a Picture. You can test these functions individually by using cabal v2-repl comp1100assignment1, using drawingOf to show small pictures on the screen. You can also test everything as a whole by launching the program with cabal v2-run shapes and pressing the S key to show the sample image. The functions you need to write for this task are all in src/View.hs:

colourNameToColour: This function turns your ColourName type from the model into a CodeWorld Colour. You should check the CodeWorld documentation for information on colours.

shapeToPicture: This function turns your Shape type into a CodeWorld Picture. You will need to consider the constructors for Shape individually, and work out the best way to turn each one into a Picture. Here are some hints to help you along:

CodeWorld has no function to draw a single line segment. It does have a function to draw a line made of multiple segments – polyline. It also has no function for triangles or ellipses, but it does have functions that can draw these shapes.

Polygons, circles, triangles, rectangles, and ellipses should be drawn as solid (filled) Pictures.

Many of CodeWorld’s functions draw individual shapes centred on the origin – (0, 0). You will need to figure out how to slide (translate) the generated Picture so it shows up where it is supposed to go. Drawing diagrams will help. The abs function might also help – it computes the absolute value of its argument (i.e., abs x == x if x &gt; 0, and abs x == – x otherwise).

Our Rectangles are defined by opposite corners. Note that there are infinitely many different rectangles who share the same pairs of opposite corners. We restrict this to only one possible rectangle by requiring that our rectangles’ vertical and horizontal edges are parallel to the $$y$$ and $$x$$ axes respectively.

Our Circles are defined by their midpoint and their radius.

Our Triangles are right-angled and isosceles, and are defined by the points at each end of the hypotenuse. As the triangle is both rightangled and isosceles, we can work out that the third point must be in one of two possible locations. To decide between these locations, assume that the points are drawn in an anti-clockwise order. e.g., if you were to draw the hypotenuse horizontally from left to right, the resultant triangle would point upwards.

Ellipses are defined by their two extremities along their major axis (the furthest apart pair of points on the edge of the ellipse), and the eccentricity, which defines how “squished” the ellipse is compared to a circle. The eccentricity is defined (for our purposes) as $$e = sqrt{1-rac{b^2}{a^2}}$$ where $$a$$ is the length of the major axis and $$b$$ the length of the minor axis. Re-arranging, we can work out that the ratio between the major and minor axes is $$rac{b}{a} = sqrt{1 – e^2}$$. You can use this information to draw an ellipse of the correct dimensions in codeworld (hint: remember that an ellipse is a squished circle). But you will have to figure out how to rotate/translate it so that the major axis aligns with the given points.

If you get stuck some of these shapes, you should move on to further exercises and then come back to them. To do this neatly, you can define a shape to be blank (no matter what its arguments are). This way, your code will compile, and it will not crash when you try to view the sample image. The harder shapes can be the hardest part of this assignment, so it can be best to do them last!

colourShapeToPicture: This function should render the Shape and colour it using the Colour that corresponds to the given ColourName.

Task 3: Handling Events (30 marks)

It is now time to tackle handleEvent in src/Controller.hs. CodeWorld calls this function whenever something interesting happens (like a key press, a pointer press, or a pointer release). This function is called with two arguments:

The Event that just happened, and

The current Model at the time the Event happened.

handleEvent then returns a new Model for the program to use moving forward.

(Aside: Elm is a functional programming language that uses a similar pattern to build front-end web applications that are compiled to JavaScript.)

Let’s trace a simple interaction. If the user wants to draw a red line by clicking on the screen at coordinates $$(1, 1)$$ and releasing the mouse at coordinates $$(2, 2)$$. starting at a blank canvas, the state would transition as follows, starting with the initial model:

1. Model [] (LineTool Nothing) Black

2. The user presses “C” to change the colour from black to red:

Model [] (LineTool Nothing) Red

1. The user presses the mouse button at $$(1, 1)$$ changing the state to

Model [] (LineTool (Just (1.0,1.0))) Red

1. The user releases the mouse button at $$(2, 2)$$ changing the state to

Model [(Line (1.0,1.0) (2.0,2.0),Red)] (LineTool Nothing) Red

{:.msg-info} Note that the Tool and the ColourName do not reset to the default values after a shape has been drawn. However, the Maybe Point inside the tool should revert to Nothing.

Task 3.1: Handling Mouse Input

CodeWorld provides a few different event constructors for mouse input, but the ones we’re interested in here are PointerPress for when the user clicks, and PointerRelease for when the user releases the mouse button.

When a PointerPress event arrives, you will need to store it in the current Tool. For everything except PolygonTool, you will store it in the Maybe Point argument. For PolygonTool, you will add it to the list of vertices.

When a PointerRelease event arrives, we can ignore it for PolygonTool, as we will be finishing polygons using the spacebar in Task 3.2. For everything else, a PointerRelease will mean the end of a click-drag-release action, so you should construct the appropriate shape and add it to the [Shape] in the Model. You should also remove the starting Point from the current Tool, so that future shapes draw properly too. It is up to you whether you should reset the eccentricity upon completing an ellipse tool.

Remember that while a circle is drawn by click-drag-release from opposite points on the circumference, it is stored as a midpoint and a radius. You will need to convert from one to the other upon pointer release.

Task 3.2: Handling Key Presses

To handle keyboard input, CodeWorld provides a KeyPress event. This is already present in the assignment skeleton, because we have implemented some keyboard functionality already. In the “Overview of the Program” section, we listed the full set of keyboard commands that your program will respond to. You need to implement the missing functionality for these keys:

| Key | Effect | |———————-|——————————————————————| | C | Change colour (of shape to draw) | |

T | Change tool (type of shape to draw) | | Backspace/Delete | Remove the last added shape | | Spacebar | Finish drawing a polygon, if it has at

Think back to Task 1.

Backspace/Delete with no shapes drawn should not crash the program.

Nor should any other unexpected input. Try to test some “unexpected” cases.

Technical Report (15 marks)

You should write a concise technical report explaining your design choices in implementing your program. The maximum word count is 1000. This is a limit, not a quota; concise presentation is a virtue.

{:.msg-warn} Once again: These are not required word counts. They are the maximum number of words that your marker will read. If you can do it in fewer words without compromising the presentation, please do so.

The report must have a title page with the following items:

Your name

Content and Structure

Introduction

If you wish to do so you can write an introduction. In it, give:

A brief overview of your program: how it works; and what it is designed to do.

what it is designed to do.

This section is particularly relevant to more complicated programs. Content

Talk about why you structured the program the way you did. Below are some questions you could answer:

Program design

Describe what each relevant function does conceptually. (i.e. how does it get you closer to solving the problems outlined in this assignment spec?)

How do these functions piece together to make the finished program? Why did you design and implement it this way?

What major design choices did you make regarding the functions that youâ€™ve written and the overall structure of your program?

Assumptions

Describe assumptions you have made about how a user might use the program and how this has influenced your design decisions.

Testing

How did you test individual functions?

Describe the tests that prove individual functions on their own behave as expected (i.e. testing a function with different inputs and doing a calculation by hand to check that the outputs are correct).

How did you test the entire program? What tests did you perform to show that the program behaves as expected in all (even unusual) cases?

Again, be specific – did you check that you can draw shapes from left to right? What about right to left, or in different vertical directions?

Inspiration / external content

What resources did you use when writing your program (e.g., published algorithms)?

If you have used resources such as a webpage describing an algorithm, be sure to cite it properly at the end of your report in a â€˜Referencesâ€™ section. References do not count to the maximum word limit.

Reflection

Discuss the reasoning behind your decisions, rather than what the decisions were. You can reflect on not only the decisions you made, but the process through which you developed the final program:

Did you encounter any conceptual or technical issues?

If you solved them, describe the relevant details of what happened and how you overcame them.

Sometimes limitations on time or technical skills can limit how much of the assignment can be completed. If you ran into a problem that you could not solve, then your report is the perfect place to describe them. Try to include details such as:

theories as to what caused the problem; suggestions of things that might have fixed it; and discussion about what you did try, and the results of these attempts.

This is a great way to gain marks to make up for a not completely successful programming experience!

What would you have done differently if you were to do it again

This means talking about if you were to write the program again – not if you were to do the assignment again. Talk about things in the program you might change (even if they go outside the spec a little bit). Do not talk about how you would change your time management or other things that are about how you did the assignment rather than how you worked on the program you are discussing in your report.

What changes to the design and structure you would make if you wrote the program again from scratch?

Are parts of the program confusing for the reader? You can explain them in the report (in this situation you should also make use of comments in your code).

If you collaborated with others, what was the nature of the collaboration? (Note that you are only allowed to collaborate by discussing concepts, not sharing solutions.)

Collaborating is any discussion or work done together on planning or writing your assignment.

Other info

{:.msg-info} This is a list of suggestions, not requirements. You should only discuss items from this list if you have something interesting to write.

Things to avoid in a technical report

Line by line explanations of large portions of code. (If you want to include a specific line of code, be sure to format as described in the “Format” section below.)

Pictures of code or your IDE.

Content that is not your own, unless cited.

Grammatical errors or misspellings. Proof-read it before submission.

Informal language – a technical report is a professional document, and as such should avoid things such as:

Unnecessary abbreviations (atm, wrt, ps, and so on), emojis, and emoticons; and

Stories / recounts of events not relevant to the development of the program.

Irrelevant diagrams, graphs, and charts. Unnecessary elements will distract from the important content. Keep it succinct and focused.

If you need additional help with report writing, ANU Academic Skills have resources to help.

Format

You are not required to follow any specific style guide (such as APA or Harvard). However, here are some tips which will make your report more pleasant to read, and make more sense to someone with a computer science background.

Colours should be kept minimal. If you need to use colour, make sure it is absolutely necessary.

If you are using graphics, make sure they are vector graphics (that stay sharp even as the reader zooms in on them).

Any code, including type/function/module names or file names, that appears in your document should have a monospaced font (such as Consolas, Courier New, Lucida Console, or Monaco)

Other text should be set in serif fonts (popular choices are Times, Palatino, Sabon, Minion, or Caslon). When available, automatic ligatures should be activated.

Do not use underscore to highlight your text.

Text should be at least 1.5 spaced.

Communicating

Sharing concepts and sketches is perfectly fine, especially with the geometry-heavy parts of the assignment, but sharing should stop before you risk handing in suspiciously similar solutions

Course staff will not look at assignment code unless it is posted privately in piazza, or shared in a drop-in consultation.

Course staff will typically give assistance by asking questions, directing you to relevant exercises from the labs, or definitions and examples from the lectures.

Submission Checklist

You have fully read and understand the entire assignment specification.

Your work has been pushed to GitLab.

Your program compiles and runs, including the cabal v2-test test suite.

You have proof-read and spell-checked your report.
