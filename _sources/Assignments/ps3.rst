:orphan:

..  Copyright (C) Paul Resnick.  Permission is granted to copy, distribute
    and/or modify this document under the terms of the GNU Free Documentation
    License, Version 1.3 or any later version published by the Free Software
    Foundation; with Invariant Sections being Forward, Prefaces, and
    Contributor List, no Front-Cover Texts, and no Back-Cover Texts.  A copy of
    the license is included in the section entitled "GNU Free Documentation
    License".

.. highlight:: python
    :linenothreshold: 500


Activities through 9/30
=======================

You have the following graded activities:

* **Before Monday's class, 9/26:**

  * Read :ref:`Conditionals <conditionals_chap>` and try exercises
  * Read :ref:`File Input/Output <files_chap>` (read the Selection/Conditionals chapter first, or the last exercise will be very confusing...)
  * Read :ref:`Understanding Code <understand_code_chap>` and do exercises

.. usageassignment

* **Before Tuesday 9/27 at 11:59 pm:**

  * Read Chapter 3 of The Most Human Human and answer `Reading Response 4 <https://umich.instructure.com/courses/105657/assignments/131315>`_ on Canvas.

* **Before Wednesday's class, 9/28:**
  
  * Read :ref:`Dictionaries<dictionaries_chap>`, and try the exercises in that chapter

.. usageassignment

* **Before Friday 9/30 at 6:30 PM:**

  * Save answers to each of the exercises in :ref:`Problem Set 3 <problem_set_3>` and submit your **Demonstrate Your Understanding** assignment to Canvas (linked in the problem set).

.. TODO basic dictionary mechanics in pset??

  * You have a grace period for the problem set and DYU submission until Sunday 10/2 at 5:00 pm.

This Week's Reading Responses
-----------------------------

.. _reading_response_4:

.. external:: rr_4

  `Reading Response 4 <https://umich.instructure.com/courses/105657/assignments/131315>`_ on Canvas.

.. _problem_set_3:

Problem Set
-----------

**Instructions:** Write the code you want to save in the provided boxes, and click **run** for each one, which will save what is in the code window. The last code you have saved for each one by the deadline is what will be graded.

.. datafile::  about_programming.txt
   :hide:

   Computer programming (often shortened to programming) is a process that leads from an
   original formulation of a computing problem to executable programs. It involves
   activities such as analysis, understanding, and generically solving such problems
   resulting in an algorithm, verification of requirements of the algorithm including its
   correctness and its resource consumption, implementation (or coding) of the algorithm in
   a target programming language, testing, debugging, and maintaining the source code,
   implementation of the build system and management of derived artefacts such as machine
   code of computer programs. The algorithm is often only represented in human-parseable
   form and reasoned about using logic. Source code is written in one or more programming
   languages (such as C++, C#, Java, Python, Smalltalk, JavaScript, etc.). The purpose of
   programming is to find a sequence of instructions that will automate performing a
   specific task or solve a given problem. The process of programming thus often requires
   expertise in many different subjects, including knowledge of the application domain,
   specialized algorithms and formal logic.
   Within software engineering, programming (the implementation) is regarded as one phase in a software development process. There is an on-going debate on the extent to which
   the writing of programs is an art form, a craft, or an engineering discipline. In
   general, good programming is considered to be the measured application of all three,
   with the goal of producing an efficient and evolvable software solution (the criteria
   for "efficient" and "evolvable" vary considerably). The discipline differs from many
   other technical professions in that programmers, in general, do not need to be licensed
   or pass any standardized (or governmentally regulated) certification tests in order to
   call themselves "programmers" or even "software engineers." Because the discipline
   covers many areas, which may or may not include critical applications, it is debatable
   whether licensing is required for the profession as a whole. In most cases, the
   discipline is self-governed by the entities which require the programming, and sometimes
   very strict environments are defined (e.g. United States Air Force use of AdaCore and
   security clearance). However, representing oneself as a "professional software engineer"
   without a license from an accredited institution is illegal in many parts of the world.


.. activecode:: ps_3_1
       :language: python

       **1.** Write code that uses iteration to print out each element of the list ``several_things``. Then, write code to print out the TYPE of each element of the list called ``several_things``.
       ~~~~
       several_things = ["hello", 2, 4, 6.0, 7.5, 234352354, "the end", "", 99]

       ====

       print "\n\n---\n"
       print "(There are no tests for this problem.)"

.. activecode:: ps_3_2
       :language: python

       **2.** See the comments for directions.
       ~~~~
       sent = "The magical mystery tour is waiting to take you away."

       # The following code does not iterate over the words in the English sentence we can read that's stored in the variable sent:
       for x in sent:
           print x
       # Why not? Knowing what you know about how computers and programming languages deal with sequences, what do you need to do to make sure you can iterate over the words in the sentence? Write a comment explaining:


       # Write code that assigns a variable word_list to hold a LIST of all the
       # WORDS in the string sent. It's fine if words include punctuation.


       =====

       from unittest.gui import TestCaseGui

       class myTests(TestCaseGui):

           def testOne(self):
               print "No tests for the comment, of course -- we can only test stored values!\n"
               self.assertEqual(word_list, sent.split(), "Testing that word_list has been set to a list of all the words in sent")

       myTests().main()

.. activecode:: ps_3_3
       :language: python

       **3.** Write code that uses iteration to print out each element of the list stored in ``excited_words``, BUT print out each element **without** its ending punctuation. You should see:

       ::

           hello
           goodbye
           wonderful
           I love Python

       (Hint: remember string slicing?)
       ~~~~

.. activecode:: ps_3_4
       :language: python

       **4.** Write code to open the file we've included in this problem set, ``about_programming.txt``, and print out each of the first two lines only. (Don't worry about blank lines appearing.) 

       **Hint:** Use one of the file methods you've learned to make this easy! Do not print out a list with ``[``s.

       The result should look like this:

       ::

           Computer programming (often shortened to programming) is a process that leads from an
  
           original formulation of a computing problem to executable programs. It involves

       :available_files: about_programming.txt
       ~~~~
       # Write your code here.
       # Don't worry about extra blank lines between each of the lines when you print them
       # (but if you want to get rid of them, you can try out the .strip() method)

       ====

       print "\n\n---\n"
       print "There are no tests for this problem."

.. activecode:: ps_3_5
       :language: python

       **5.** Write code to open the file ``about_programming.txt`` and assign the **number of lines** in the file to the variable ``file_lines_num``.

       :available_files: about_programming.txt
       ~~~~
       # Write your code here.

       =====

       from unittest.gui import TestCaseGui

       class myTests(TestCaseGui):

          def testOne(self):
             print "No tests for the comment, of course -- we can only test stored values!\n"
             self.assertEqual(file_lines_num,len(open("about_programming.txt","r").readlines()), "Testing to see that file_lines_num has been set to the number of lines in the file.")

       myTests().main()


.. activecode:: ps_3_6
       :language: python

       **6.** The program below doesn't always work as intended. Try uncommenting different lines setting the initial value of x. Tests will run at the end of your code, and you will get diagnostic error messages. 

       Fix the code so that it passes the test for each different value of x. So when the first line is uncommented, and when the second line, third line, and fourth line are each uncommented, you should always pass the test.

       (HINT: you don't have to make a big change.)
       ~~~~ 
       #x = 25
       #x = 15
       #x = 5
       #x = -10

       if x > 20:
           y = "yes"
       if x > 10:
           y = "no"
       if x < 0:
           y = "maybe"
       else:
           y = "unknown"

       print "y is " + str(y)

       =====

       from unittest.gui import TestCaseGui

       class myTests(TestCaseGui):

           def testOne(self):
               print("No tests for the comment, of course -- we can only test stored values!\n")
               if x == 25:
                   self.assertEqual(y, "yes", "test when x is 25: y should be 'yes'")
               elif x == 15:
                   self.assertEqual(y, 'no', "test when x is 15: y should be 'no'")
               elif x == 5:
                   self.assertEqual(y, 'unknown', "test when x is 5: y should be 'unknown'")
               elif x == -10:
                   self.assertEqual(y, 'maybe', "test when x is -10: y should be 'maybe'")
               else:
                   print "No tests when value of x is %s" % (x)

       myTests().main()


.. activecode:: ps_3_7
       :language: python

       **7.** How many characters are in each element of list ``lp``? Write code to print the length (number of characters) of each element of the list, on a separate line. (Do not write 8+ lines of code to do this. Use a for loop.)

       The output you get should be:

       :: 

           5
           13
           11
           12
           3
           12
           11
           6 

       Then, write code to print out each element of list ``lp`` *only if* the length of the element is an even number. Use iteration (a for loop!).
       ~~~~
       lp = ["hello","arachnophobia","lamplighter","inspirations","ice","amalgamation","programming","Python"]
       ====

       print "\n---\n\n"
       print "There are no tests for this problem."

.. activecode:: ps_3_8
       :language: python

       **8.** Write code to count the number of strings in list ``items`` that have the character ``w`` in it. Assign that number to the variable ``acc_num``. 

       HINT 1: Use the accumulation pattern! 

       HINT 2: the ``in`` operator checks whether a substring is present in a string.
       ~~~~
       items = ["whirring", "calendar", "wry", "glass", "", "llama","tumultuous","owing"]
       =====

       from unittest.gui import TestCaseGui

       class myTests(TestCaseGui):

           def testOne(self):
               self.assertEqual(acc_num, 3, "Testing that acc_num has been set to the number of strings that have 'w' in them.")

       myTests().main()

.. activecode:: ps_3_9
       :language: python

       **9.** Below is a dictionary ``diction`` with two key-value pairs inside it. The string ``"python"`` is one of its keys. Using dictionary mechanics, print out the value of the key ``"python"``.
       ~~~~
       diction = {"python":"you are awesome","autumn":100}

       # Write your code here.

       ====

       print "\n\n---\n"
       print "There are no tests for this problem."

.. activecode:: ps_3_10
       :language: python

       **10. Challenge problem (OPTIONAL):** write code to find the average (mean) number of words in each line of the file ``about_programming.txt``.

       :available_files: about_programming.txt
       ~~~~
       # Write your code here.

       ====

       print "\n\n---\n"
       print "There are no tests for this problem."

.. external:: ps3_dyu

  Submit your `Demonstrate Your Understanding <https://umich.instructure.com/courses/105657/assignments/131286>`_ for this week on Canvas.