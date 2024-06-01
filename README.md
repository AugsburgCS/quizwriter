# Quiz Quiz Quiz Writer
by Amy C. Larson, Ph.D. <br>
Computer Science <br>
Augsburg University in Minneapolis, MN

<hr>
I claim this content to be my property, but I am happy to share. Feel free to use and modify for your courses!
<hr>

This latex framework can be used to relatively easily write multiple versions of a paper quiz. It is definitely under development. However, I am using it for my course so it is functional! p.s. I develop everything in Overleaf.



Let me preempt a question that is bound to arise -- one that I see as a response on the web to many coding inquiries.

	"Why did you do it that way? It is so much easier if you use X."
	
My response is either:

1. "A person can use only those language constructs that they know, which is a product of their experience and time available to learn. Likely, if there was a better way and I knew that better way, then I would use it."

2. "I think my way is better for some reason. Some reasons include it is more transparent and/or easier to read and/or easier to use and/or quicker for me to write it with what I know than to study a 100 page manual to figure out someone else's logic."

I am a very experienced programmer, but a novice at Latex. I waged many battles with Latex over this framework, and I thank the web community at large for at least trying to explain things and to provide examples. 

I also note that I know there are many awesome latex packages and classes out there to generate exams, quizzes, and exercises, many of which are built on top of the _exam_ class explained here: https://math.mit.edu/~psh/exam/examdoc.pdf. I have looked at the descriptions of many, and I have not found a good match for what I am trying to do, but please let me know if that is not the case. And note that the author of the _exam_ class states it " ... attempts to make it easy for even a LATEX novice to prepare exams," which is the opening sentence of a 135 page user manual.

Many of the examples that I see on the web to explain this or that in Latex are from those deeply knowledgeable in the language -- they forgot what it is like not to know what they know. One of my goals is to make this as transparent as possible, thus I have heavily commented the code. I try to indicate where I know there must be an easier way, but I don't have time to figure it out (after all, it is working -- well sort of).

## Create Your Own Quizzes

As the USER of this quiz writer, you have 4 jobs ...

1. Create a folder for the quiz you want to create.

2. Create a file for each question inside that folder. Each question has a preamble, postamble, and versions. You can look at the question files in basic example to see how this is structured.

3. Create the setup file that identifies questions and quiz versions. Look at the setup file in the basicexample folder.

4. Set the qfolder (quiz folder) and qsetup (quiz setup file) variables to correspond to the folder/files you created above.

The only lines (hopefully) that you have to change in main.tex are defining qfolder and qsetup:

```
% _____________ USER DEFINED folder and setup file ___________
% specify which folder contains questions for the quiz
% specify which file in this folder contains setup information


\def\qfolder{functions}   % << YOU SET THIS
\def\qsetup{quizsetup}  % << YOU SET THIS
```

Each time you create a new quiz folder, you can change the folder name above and recompile to generate the quizzes.

## Use Provided Quizzes 

I have provided a collection of quizzes that I use in Introduction to Programming (Python). Feel free to use them in your courses.

## It Works, Eventually

I compile in Overleaf, which happily ignores all of my mistakes. If you do command-line compilation with `pdflatex`, keep hitting the return and the compiler will eventually relent and produce a pdf!

I think most of my problems can be attributed to the timing of the expansion of the various commands that are defined. Let me know if you know how to fix something or if you know something I should really know about. Thanks in advance!



