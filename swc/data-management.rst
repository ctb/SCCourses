A Quick Guide to Organizing Computational (Biology) Projects
================================================================================

----

In Short ...
--------------------------------------------------------------------------------

.. raw:: html

  <span class="big">

- Poor organizational choices lead to significantly slower research progress.
- It is critical to make your results reproducable.

.. raw:: html

   </span>

.. This presentation is based on Bill Noble's "A quick guide to organizing
.. computational biology projects". 

.. Bioinformatics courseworks, as many other scientific courseworks focus on
.. algorithms or bioinformatics software. Unfortunately, these course fail to
.. prepare students for day to day organizational challenges in a research
.. carreer. In this talk, I will present Bill Noble's strategy, some of Greg
.. Wilson's software carpentry tips, and Buckheit and Donoho's experience
.. concerning data management and experiments organizations 

.. Poor organization and poor software practices lead to significantly slower
   research progress. I will start by quoting extracts of Buckheit's and
   Donoho's paper on reproducible science, to underline the importance of good
   practices.

----

The Stolen Briefcase
--------------------------------------------------------------------------------

  "Once, several years ago, at a conference, one of us had a briefcase stolen.
  The briefcase contained originals figure which had been developed while an
  employee of a large commercial seismic exploration outfit. [..] A manuscript
  had already been written. The figures were so convincing and pivotal [..] that
  without them, the manuscript made no sense. **The manuscript had to be
  abandoned.**"

----

Who's one First?
--------------------------------------------------------------------------------

  "A Graduate Student comes into a Professor's office and says, "That idea you
  told me to try - it doesn't work!". [..] Unfortunately, the **Student's
  descriptions of the problems he is facing don't give the Professor much
  insight on what's going on.**"

----

A year is time long in this business
--------------------------------------------------------------------------------

  "When he went back to the old software library [..], **he couldn't remember
  how the software worked** - invocation of sequences, data structures, etc. in
  the end, he abandonned the project, saying he just didn't have time to get
  into it anymore."

----

A la recherche des paramètres perdues
--------------------------------------------------------------------------------

  "Well, actually, the reason we didn't give many details in the paper is that
  we forgot which parameters gave the nice pictures you see in the published
  article; when we tried to reconstruct that figure using parameters that we
  thought had been used, we only got ugly looking results. So we knew there
  had been some parameter settings which worked well, and perhaps on day we
  would stumble on them again; but we thought it best to leave things vague"

(note: this story is actually a composite of two separate true incidents)

----

Principles
--------------------------------------------------

----

First Principle
--------------------------------------------------------------------------------

.. raw:: html

     <blockquote class="medium">

"Someone unfamiliar with your project should be able to look at your
computer files and understand in detail what you did and why."

.. raw:: html

     </blockquote>


----

Second Principle
-------------------------------------------------------------------------------

.. raw:: html

     <blockquote class="medium">

"Everything you do, you will have to do over and over again"

.. raw:: html

     </blockquote>

-- Murphy's law

----

File and directory  organization
---------------------------------

----

So far, so good...
--------------------------------------------------------------------------------

.. image:: https://github.com/ctb/SCCourses/raw/master/swc/images/01_files.png
  :scale: 60%

----

Now what ?
--------------------------------------------------------------------------------

.. image:: https://github.com/ctb/SCCourses/raw/master/swc/images/02_files.png
  :scale: 60%

----

I guess this is alright
--------------------------------------------------------------------------------

.. image:: https://github.com/ctb/SCCourses/raw/master/swc/images/03_files.png
  :scale: 60%

----

Which one is the most recent?
--------------------------------------------------------------------------------

.. image:: https://github.com/ctb/SCCourses/raw/master/swc/images/04_files.png
  :scale: 60%

----

Another (bad) common approach
--------------------------------------------------------------------------------

.. image:: https://github.com/ctb/SCCourses/raw/master/swc/images/another_common_approach.png
  :scale: 60%

----

A (possible) solution
--------------------------------------------------------------------------------

.. image:: https://github.com/ctb/SCCourses/raw/master/swc/images/correct_.png
  :scale: 60%

----

Still missing something...
--------------------------------------------------------------------------------

- We give the project to a collaborator
- A new student joins the project
- 3 years later, haven't we forgotten the details of the projects?


We need **context**. We need **metadata**.

----

Metadata
--------------------------------------------------------------------------------

- who is the data from?
- when was it generate?
- what were the experiment conditions?

.. image:: https://github.com/ctb/SCCourses/raw/master/swc/images/data.gif

----

Project organisation
--------------------------------------------------------------------------------

.. image:: https://github.com/ctb/SCCourses/raw/master/swc/images/project_organization.png
  :scale: 60%

----

The lab notebook
--------------------------------------------------

----

What is it?
--------------------------------------------------------------------------------

  "A laboratory notebook (colloq. lab notebook) is a primary record of research.
  Researchers use a lab notebook to document their hypotheses, experiments and
  initial analysis or interpretation of these experiments. The notebook serves
  as an organizational tool, a memory aid, and can also have a role in
  protecting any intellectual property that comes from the research."

      -- Wikipedia

----

The notebook
--------------------------------------------------------------------------------

- entries should be dated
- verbose, links or embedded images, tables
- results of all the experiments performed


----

Carrying out a Single Experiment
--------------------------------------------------

----

Experiments
------------

- record all operations you do, in order to make those operations transparents
  and reproducable.
- in practice, create a README, in which you store every command line you use

----

6 steps
---------

- Record every operation you perform
- Comment generously
- Avoid editing intermediate files by hand
- Store all files and directory names in the script
- Use relative pathnames to access files within the same project
- Make the script restartable

----

Handling and preventing errors
--------------------------------------------------

----

Bugs...
--------------------------------------------------------------------------------

.. raw:: html

  <span class="big">

You **will** introduce errors into your code

.. raw:: html

   </span>

.. image:: https://github.com/ctb/SCCourses/raw/master/swc/images/bug.png



-----

3 suggestions for error handling
--------------------------------------------------------------------------------

- Write robust code to detect errors
- When an error occurs abort
- Whenever possible, create an output file using a temporary name, and rename
  the file when the script is complete

----

Command line vs script vs program
--------------------------------------------------

----

Software engineering
--------------------------------------------------------------------------------

.. image:: https://github.com/ctb/SCCourses/raw/master/swc/images/good_code.png
   :scale: 70%

----

4 types of script
--------------------------------------------------------------------------------

- Driver script:
- Single use script: data format conversion
- Project specific script: contains a generic functionality used by multiple
  experiments
- Multi projects script: functionnalities used across many projects (ROC
  curve, n-fold cross validation, etc).

----

The Value of Version Control
--------------------------------------------------------------------------------

----

.. image:: https://github.com/ctb/SCCourses/raw/master/swc/images/stolen_briefcase.png

----

Thanks for your attention
--------------------------------------------------------------------------------
