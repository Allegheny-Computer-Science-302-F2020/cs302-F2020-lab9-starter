# cs302-F2020-lab9-starter

![](../../workflows/build/badge.svg)

## Table of Contents

* [Objectives](#objectives)
* [Introduction](#introduction)
* [Continuous Learning](#continuous-learning)
* [Assignment Reminders](#assignment-reminders)
* [Accessing the Assignment](#accessing-the-assignment)
* [Laboratory Assignment Tasks](#laboratory-assignment-tasks)
  + [Using JavaScript to Support Dynamic Font Loading](#using-javascript-to-support-dynamic-font-loading)
  + [Running a Web Server](#running-a-web-server)
  + [Reflecting on the Laboratory Assignment](#reflecting-on-the-laboratory-assignment)
  + [Transferring Your Source code and Technical Writing to GitHub](#transferring-your-source-code-and-technical-writing-to-github)
* [Automated Checks with GatorGrader](#automated-checks-with-gatorgrader)
* [Assignment Assessment](#assignment-assessment)
* [Advance Feedback on an Assignment](#advance-feedback-on-an-assignment)
* [Discussion of a Graded Assignment](#discussion-of-a-graded-assignment)
* [Additional System Resources](#additional-system-resources)
  + [System Commands](#system-commands)
  + [Non-Interactive Docker Commands](#non-interactive-docker-commands)
  + [Commands for an Interactive Docker Shell](#commands-for-an-interactive-docker-shell)
  + [Upgrading the Docker Container](#upgrading-the-docker-container)
  + [Downloading Project Updates](#downloading-project-updates)
  + [Using GitHub Actions](#using-github-actions)
  + [System Requirements](#system-requirements)
* [Reporting Problems](#reporting-problems)
* [Receiving Assistance](#receiving-assistance)

## Objectives

The learning objectives for this laboratory assignment are as follows:

- To use a Docker container to run the automated checks performed by GatorGrader
- To use a terminal window to run a web server through a Python program and observe its output
- To write JavaScript that dynamically generates HTML content
- To connect HTML, JavaScript, and CSS file in a correct fashion
- To use JavaScript and AJAX to perform dynamic font loading on a web page
- To draw a technical diagram that shows the connection between HTML, CSS, and JavaScript
- To add a graphics file to a project's GitHub repository

## Introduction

Designed for use with [GitHub Classroom](https://classroom.github.com/) and
[GatorGrader](https://github.com/GatorEducator/gatorgrader/), this repository
contains a laboratory assignment for a web development course. The source code
and technical writing for this assignment must pass tests set by the
[GatorGrader tool](https://github.com/GatorEducator/gatorgrader). When you use
the `git commit` command to transfer your source code to your GitHub
repository, GitHub Actions will initialize a build of your assignment, checking
to see if it meets all of the requirements. If both your source code and
writing meet all of the established requirements, then you will see a green ✔
in the listing of commits in GitHub. If your submission does not meet the
requirements, a red ❌ will appear instead. Please note that, at the option of
the course instructor, some checks may be run in GitHub Actions that are not
run locally by the [GatorGrader
tool](https://github.com/GatorEducator/gatorgrader).

## Continuous Learning

If you have not done so already, please read all of the relevant [GitHub
Guides](https://guides.github.com/) that explain how to use many of the features
that GitHub provides. In particular, please make sure that you have read the
following GitHub guides: [Mastering
Markdown](https://guides.github.com/features/mastering-markdown/), [Hello
World](https://guides.github.com/activities/hello-world/), and [Documenting Your
Projects on GitHub](https://guides.github.com/features/wikis/). Each of these
guides will help you to understand how to use both [GitHub](http://github.com) and
[GitHub Classroom](https://classroom.github.com/).

Students who want to learn more about how to use
[Docker](https://www.docker.com) should review the [Docker
Documentation](https://docs.docker.com/). Students are also encouraged to
review the documentation for their text editor, which is available at [VS
Code](https://code.visualstudio.com/docs). You should also review the [Git
documentation](https://git-scm.com/doc) to learn more about how to use the Git
command-line client. In addition to talking with the instructor and technical
leader for your course, students are encouraged to search
[StackOverflow](https://stackoverflow.com/) for answers to their technical
questions.

As outlined in the course schedule in the [course planning
repository](https://github.com/Allegheny-Computer-Science-302-F2020/cs302-F2020-plans),
students should also read all of the assigned readings for up to and including
the week of the semester on which this laboratory assignment was assigned.

## Assignment Reminders

- **Follow each step carefully**. Slowly read each sentence in this document,
  making sure that you precisely follow each instruction. Take notes about each
  step that you attempt, recording your questions and ideas and the challenges
  that you faced. If you are stuck, then please tell a technical leader or the
  course instructor what assignment step you recently completed.

- **Regularly ask and answer questions**. Please log into Slack at the start of
  the laboratory session and then join the appropriate channel. If you have a
  question about one of the steps in an assignment, then you can post it to the
  designated channel, discussing your questions through both Slack and the
  Google Meet designated for the class.

- **Store your files in GitHub**. Starting with this laboratory assignment, you
  will be responsible for storing all of your files (e.g., Python source code
  and Markdown-based writing) in a Git repository using GitHub Classroom. Please
  verify that you have saved your source code in your Git repository by using
  `git status` to ensure that everything is updated. You can see if your
  assignment submission meets the established correctness requirements by using
  the provided checking tools on your local computer and by checking the commits
  in GitHub.

- **Keep all of your files**. Don't delete your programs, output files, and
  written reports after you submit them through GitHub; you will need them
  again when you study for the course assessments and work on the other
  laboratory, practical, and technical challenge assignments.

- **Hone your technical writing skills**. Computer science assignments require
  to you write technical documentation and descriptions of your experiences when
  completing each task. Take extra care to ensure that your writing is
  interesting and both grammatically and technically correct, remembering that
  computer scientists must effectively communicate and collaborate with their
  team members and the student technical leaders and course instructor.

- **Review the Honor Code on the syllabus**. While you may discuss your
  assignments with others, copying source code or technical writing is a
  violation of Allegheny College's Honor Code.

## Accessing the Assignment

To access this assignment, you should go into the `#announcements` channel in
our Slack workspace and find the announcement that provides a link for it. Copy
this link and paste it into your web browser. Now, you should accept the
laboratory assignment and see that GitHub Classroom created a new GitHub
repository for you to access the assignment's starting materials and to store
the completed version of your assignment. Specifically, to access your new
GitHub repository for this assignment, please click the green "Accept" button
and then click the link that is prefaced with the label "Your assignment has
been created here". If you accepted the assignment and correctly followed these
steps, you should have created a GitHub repository with a name like
`Allegheny-Computer-Science-302-Fall-2020/computer-science-302-fall-2020-lab-9-gkapfham`.
Unless you provide the course instructor with documentation of the extenuating
circumstances that you are facing, not accepting the assignment means that you
automatically receive a failing grade for all of its components.

Before you move to the next step of this laboratory assignment, please make sure
that you read all of the content on the web site for your new GitHub repository,
paying close attention to the technical details about the commands that you will
type and the output that your program must produce. Now you are ready to
download the starting materials to your laboratory computer. Click the "Clone or
download" button and, after ensuring that you have selected "Clone with SSH",
please copy this command to your clipboard. At this point, you can open a new
terminal window and type the command `mkdir cs302F2020`. To enter into this
directory you should now type `cd cs302F2020`. Next, you can type the either
`ls` (on either MacOS or Linux) or `dir` (on Windows 10 Pro or Windows 10
Enterprise) and see that there are no files or directories inside of this
directory. By typing `git clone` in your terminal and then pasting in the string
that you copied from the GitHub site you will "download" all of the code for
this assignment. For instance, if the course instructor ran the `git clone`
command in the terminal, it would look like:

```
git clone git@github.com:Allegheny-Computer-Science-302-F2020/computer-science-302-fall-2020-lab-9-gkapfham.git
```

After this command finishes, you can use `cd` to change into the new directory.
If you want to "go back" one directory from your current location, then you can
type the command `cd ..`. Finally, please continue to use the `cd` and `ls`
commands to explore the files that you automatically downloaded from GitHub. If
one of the aforementioned commands does not work correctly, then it is possible
that your terminal window is not up-to-date or not configured correctly. In this
case, please share your specific error messages with the instructor, ultimately
working to master the use of terminal commands. What files and directories do
you see? What do you think is their purpose? Spend some time exploring, telling
your discoveries to a student technical leader.

## Laboratory Assignment Tasks

### Using JavaScript to Support Dynamic Font Loading

This laboratory assignment invites you to learn how to use JavaScript to
automatically apply a Google web font to the body text inside of a web page. The
idea is that the click of a button should cause all of the body text within the
page to change to the font designated by the label on the button. After you
study the provided source code, you should notice that the source code is
implemented so that it should work regardless of the chosen web fonts. As such,
please modify the provided code so that it works with four new Google web fonts
that are not currently specified in the `index.html` file. Don't forget to test
your program, ensuring that you use the following source code, in your HTML
file, to load the needed JavaScript files. If you are not sure what source code
you need to provide, please follow the `TODO` markers to understand what is
needed.

After you run your web server by following the instructions in the following
section, you should check to see if your web site looks correct. If it is not,
then continue to edit and check it until the files are correct. You should also
ensure that, when you run the web server, it produces output suggesting that it
is returning the correct files and images. If not, then please make sure that
you revise your HTML, JavaScript, and CSS source code and/or check the
configuration of your web server. Finally, when you are studying your web site
you should verify the correctness of all its components by interacting with all
of the buttons on the site and confirming that the font changes take place.
Don't forget to try your web site in different browsers to confirm that the
feature that you implemented works in a cross-browser fashion!

### Running a Web Server

Your GitHub repository contains a directory called `www/` in the directory
called `src/`. You can run the Python-based web server and point it to the
`src/www/` directory, which will ultimately result in the creation of a web
site that features three HTML files.

```
python -m http.server --directory src/www
```

When you look in your terminal window after accessing the file served by this
HTTP server you should see some debugging output. Can you explain what this
output means? What output do you see in your terminal window? Please make sure
that you record this output in your reflection, as described further in the next
section of this document.

### Reflecting on the Laboratory Assignment

Once you have finished both of the previous technical tasks, use your text
editor to answer all of the questions in the `writing/reflection.md` file. For
instance, answer all of the other questions about your experiences in completing
this laboratory assignment. Specifically, the writing assignment for this
laboratory assignment invites you create a technical diagram using a web-based
diagram creation tool, export that diagram to a portable network graphic (PNG)
file, and then commit it to your GitHub repository. After adding Markdown source
code that will link to the technical diagram, please make sure that you furnish
additional writing that explains the provided technical diagram. You should also
answer questions about how JavaScript statements and functions support the
dynamic font loading process.

### Transferring Your Source code and Technical Writing to GitHub

As you are working on your laboratory assignment, please make sure that you use
VSCode to regularly save your work and transfer it to the GitHub servers. For
instance, please use the `git commit` command in your terminal window or use the
similar feature in VSCode to "stage" your changes in your repository. Once you
have committed your source code to your repository, you can use the `git push`
command to transfer your work to your GitHub repository, making it available for
the course instructor to assess. Please make sure that you regularly commit your
source code and technical writing, using descriptive commit messages to explain
how each commit changes the contents of the repository. Please do not use
vacuous commit messages that do not explain how your commit changes the contents
of the repository!

## Automated Checks with GatorGrader

In addition to meeting all of the requirements outlined in this assignment
sheet, your submission must pass the following checks that
[GatorGrader](https://github.com/GatorEducator/gatorgrader) automatically
assesses:

- The command `htmlhint src/www/*.html` executes correctly
- The command output has exactly 1 lines
- The file fontchange.js exists in the src/www/js directory
- The file index.html exists in the src/www/ directory
- The file javascript_submission.png exists in the images directory
- The file reflection.md exists in the writing directory
- The file web_site_connections.png exists in the images directory
- The index.html in src/www/ has at least 1 of the `ajax.googleapis.com` fragment
- The index.html in src/www/ has at least 1 of the `<body>` fragment
- The index.html in src/www/ has at least 1 of the `<head>` fragment
- The index.html in src/www/ has at least 1 of the `<html>` fragment
- The index.html in src/www/ has at least 1 of the `js/fontchange.js` fragment
- The index.html in src/www/ has at least 1 of the `<title>Dynamic Font Loading</title>` fragment
- The index.html in src/www/ has at least 1 of the `webfont.js` fragment
- The index.html in src/www/ has at least 1 of the `wrapper` fragment
- The index.html in src/www/ has at least 4 of the `button data-font` fragment
- The index.html in src/www/ has exactly 0 of the `Add Your Name Here` fragment
- The index.html in src/www/ has exactly 0 of the `TODO` fragment
- The reflection.md in writing has at least 1 of the `code` tag
- The reflection.md in writing has at least 1 of the `(images/web_site_connections.png)` fragment
- The reflection.md in writing has at least 300 word(s) in total
- The reflection.md in writing has at least 3 of the `code_block` tag
- The reflection.md in writing has exactly 0 of the `Add Your Name Here` fragment
- The reflection.md in writing has exactly 0 of the `TDO` fragment
- The reflection.md in writing has exactly 0 of the `TOD` fragment
- The reflection.md in writing has exactly 0 of the `TODO` fragment
- The reflection.md in writing has exactly 8 of the `heading` tag
- The repository has at least 5 commit(s)

```
        ┏━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━┓
        ┃ Passed 28/28 (100%) of checks for cs302-F2020-lab9! ┃
        ┗━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━┛
```

If [GatorGrader's](https://github.com/GatorEducator/gatorgrader) automated
checks pass correctly, the tool will produce the output like the following in
addition to returning a zero exit code (which you can access by typing the
command `echo $?`). You will need to run
[GatorGrader](https://github.com/GatorEducator/gatorgrader) in a Docker
container by following the steps in the sections that explain how to use Docker.

## Assignment Assessment

Taking inspiration from the principles of [specification-based
grading](https://www.amazon.com/Specifications-Grading-Restoring-Motivating-Students/dp/1620362422),
the grade that a student receives on a laboratory assignment will be based on
whether or not it meets the standards for technical work in the fields of
software engineering and discrete structures. Instead of receiving a single
numerical or letter grade for this assignment, your grade will have the
following components:

- **Percentage of Correct GatorGrader Checks Ranging Between 0 and 100**: Your
  submitted Python program must pass all of GatorGrader's checks by, for
  instance, ensuring that it produces the correct output and has all of the
  required characteristics. Your technical writing must pass all of
  GatorGrader's checks about, for instance, the length of its output and its use
  of the required Markdown language features for technical writing. For this
  component of a laboratory assignment's grade, your work will receive a
  percentage, ranging from 0 to 100, that corresponds to the percentage of
  GatorGrader checks that automatically pass inside of a GitHub Actions build.

- **GitHub Actions Build Status of Either ✔  or ❌**: Since additional checks on
  the Python source code and/or technical writing are encoded in GitHub Action
  workflows and, moreover, all of the GatorGrader checks are also run in GitHub
  Actions, your work will receive a checkmark grade if the last
  before-the-deadline build in GitHub Actions passes and a ✔  appears in the
  GitHub commit log instead of an ❌. The build status reported by GitHub
  Actions will only be a ✔ if the source code and technical writing in the
  GitHub repository pass all of both the GatorGrader checks and the additional
  checks.

- **Technical Writing Mastery of Either ✔  or ❌**: Students will also receive a
  ✔ grade when the responses to the technical writing questions presented in the
  `writing/reflection.md` reveal a mastery of technical writing skills. To
  receive a checkmark grade, the submitted writing should have correct spelling,
  grammar, punctuation, and formatting in addition to following the rules of the
  Markdown language. Your work will receive a ✔ grade for this component
  if the build report from GitHub Actions reveals that there are no detected
  mistakes in the technical writing.

- **Technical Knowledge and Skill Mastery of Either ✔  or ❌**: Students will
  also receive a checkmark grade when the GitHub repository reveals that they
  have mastered all of the technical knowledge and skills developed during the
  completion of the laboratory assignment. As a part of this grade, the
  instructor will assess aspects of the project including, but not limited to,
  the use of effective Python source code comments, correct Git commit messages,
  and accurate responses to the technical writing questions.

## Advance Feedback on an Assignment

Students who wish to receive feedback on their work for any course assignment
should first open an issue on the issue tracker for their assignment's GitHub
repository, giving an appropriate title and description for the type of feedback
that you would like the course instructor to provide. After creating this issue,
you will see that GitHub has created a unique web site that references it. To
alert the course instructor to the fact that the issue was created and that you
want feedback on your work, please send it to him by a Slack direct message at
least 24 hours in advance of the project's due date. After the instructor
responds to the issue, please resolve all of the stated concerns and participate
in the discussion until the issue is resolved and ultimately marked as closed.

## Discussion of a Graded Assignment

Students who wish to receive feedback on their work for any graded course
assignment should leave question in the same region of Github where the course
instructor submitted the assignment's grade. For example, if the instructor
submits your grade to a pull request in your repository for a laboratory
assignment, then you should ask questions about your grade in that pull request,
bearing in mind the need to @-mention the course instructor in the body of your
comment. Students can continue to discuss the graded assignment with the course
instructor until they understand all the technical topics that were the
focus of the particular assignment.

## Additional System Resources

### System Commands

This project invites students to enter system commands into a terminal window.
This assignment uses [Docker](https://www.docker.com) to deliver programs, such
as `gradle` and the source code and packages needed to run
[GatorGrader](https://github.com/GatorEducator/gatorgrader), to a students'
computer, thereby eliminating the need for a programmer to install them on their
development workstation. Individuals who do not want to install Docker can
optionally install of the programs mentioned in the [Project
Requirements](#requirements) section of this document.

### Non-Interactive Docker Commands

Once you have installed [Docker
Desktop](https://www.docker.com/products/docker-desktop), with MacOS and Linux
you can use the following `docker run` command to start `gradle grade` as a
containerized application, using the
[DockaGator](https://github.com/GatorEducator/dockagator) Docker image available
on
[DockerHub](https://cloud.docker.com/u/gatoreducator/repository/docker/gatoreducator/dockagator).

```bash
docker run --rm --name dockagator \
  -v "$(pwd)":/project \
  -v "$HOME/.dockagator":/root/.local/share \
  gatoreducator/dockagator
```

The aforementioned command will use `"$(pwd)"` (i.e., the current working
directory) as the project directory and `"$HOME/.dockagator"` as the cached
GatorGrader directory. Please note that both of these directories must exist,
although only the project directory must contain something. Generally, the
project directory should contain the source code and technical writing for an
assignment, as provided to a student by the instructor through GitHub.
Additionally, the cached directory should not contain anything other than
directories and programs created by DockaGator, thus ensuring that they are not
otherwise overwritten during the completion of the assignment.

To ensure that the previous command will work correctly, you should create the
cache directory by running the command `mkdir $HOME/.dockagator` on the MacOS
and Linux operating systems. However, if you are using the Windows operating
system then you will instead need to type the command `mkdir
%HomeDrive%%HomePath%/.dockagator`. Finally, since the above `docker run`
command does not work correctly on the Windows operating system, you will need
to instead run the following command to adapt to the differences in the `cmd`
terminal window:

```bash
docker run --rm --name dockagator \
  -v "%cd%:/project" \
  -v "%HomeDrive%%HomePath%/.dockagator:/root/.local/share" \
  gatoreducator/dockagator
```

Please note that not all version of the Windows terminal window will correctly
recognize the use of the `%cd%` and `%HomeDrive%%HomePath%` variables. In this
case, you should substitute the actual directory for a specific course
assignment for the `%cd%` variable and the drive letter that contains the
`.dockagator` directory for the `%HomeDrive%%HomePath%` variable. Finally, the
Windows terminal window may not work correctly when you attempt to run a
multi-line command. In this case, you should break up the aforementioned
four-line command into separate lines, like `docker run --rm --name dockagator`
and `-v "%cd%:/project"` and then connect them into a single long line that you
separate by a single space. Here is an example of what the long command would
look like, again assuming that the Windows `cmd` terminal correctly interprets
the `%cd%` and `%HomeDrive%%HomePath%` variables:

```bash
docker run -it --rm --name dockagator -v "%cd%:/project" -v "%HomeDrive%%HomePath%/.dockagator:/root/.local/share" gatoreducator/dockagator /bin/bash
```

Here are some additional commands that you may need to run when using Docker:

* `docker info`: display information about how Docker runs on your workstation
* `docker images`: show the Docker images installed on your workstation
* `docker container list`: list the active images running on your workstation
* `docker system prune`: remove many types of "dangling" components from your workstation
* `docker image prune`: remove all "dangling" docker images from your workstation
* `docker container prune`: remove all stopped docker containers from your workstation
* `docker rmi $(docker images -q) --force`: remove all docker images from your workstation

### Commands for an Interactive Docker Shell

Since the above `docker run` command uses a Docker images that, by default, runs
`gradle grade` and then exits the Docker container, you may want to instead run
the following command so that you enter an "interactive terminal" that will
allow you to repeatedly run commands within the Docker container. Don't forget
that, if you are using the Windows operating system, then you will need to use a
different command to run Docker, as explained previously in this document.
Importantly, the command that you type if you are a Windows user should still
contain the `-it` at the start of the `docker run` and the `/bin/bash` at the
end of the command. However, the other components of this command need to be
customized for the Windows operating system.

If you use either MacOS or Linux, then this is the command that you would run to
enter into the interactive terminal provided by a Docker container:

```bash
docker run -it --rm --name dockagator \
  -v "$(pwd)":/project \
  -v "$HOME/.dockagator":/root/.local/share \
  gatoreducator/dockagator /bin/bash
```

If you use Windows, then this is the command that you would run to enter into
the interactive terminal provided by a Docker container:

```bash
docker run -t --rm --name dockagator \
  -v "%cd%:/project" \
  -v "%HomeDrive%%HomePath%/.dockagator:/root/.local/share" \
  gatoreducator/dockagator /bin/bash
```

Once you have typed this command, you can use the [GatorGrader
tool](https://github.com/GatorEducator/gatorgrader) in the Docker container by
typing the command `gradle grade` in your terminal. Running this command will
produce a lot of output that you should carefully inspect. If GatorGrader's
output shows that there are no mistakes in a course assignment, then your source
code and technical writing are passing all of the automated baseline checks.
However, if the output indicates that there are mistakes, then you will need to
understand what they are and then try to fix them.

Remember, to correctly run any of the commands mentioned in this guide, you must
be in the main (i.e., "home base") directory for a course assignment where the
`build.gradle` file is located.

### Upgrading the Docker Container

If the course instructor provides a new version of the Docker container called
`gatoreducator/dockagator` and you want to receive it immediately, you must
first delete the existing Docker container on your laptop by running the command
`docker rmi gatoreducator/dockagator`. Next, you can re-run one of the
aforementioned Docker commands, like the following one, which would work on
MacOS or Linux:

```
docker run -it --rm --name dockagator \
  -v "$(pwd)":/project \
  -v "$HOME/.dockagator":/root/.local/share \
  gatoreducator/dockagator /bin/bash
```

Please note that if you attempt to run `gradle grade` in an updated Docker
container it is possible that the command will execute incorrectly if you
previously used GatorGrader with a Docker container that featured a different
version of the Python programming language. In this situation, you should delete
the directories inside of the `.dockagator` directory and then again attempt to
run the `gradle grade` command inside of the Docker container. Specifically, you
will need to delete directories in `.dockagator` that are normally called
`gatorgrader`, `virtualenv`, and `virtualenvs`.

### Downloading Project Updates

If the course instructor pushes updates to this assignment and you received it
through GitHub Classroom and you would like to also receive these updates, then
you can type this command in the main directory for this assignment:

```
git remote add download git@github.com:Allegheny-Computer-Science-302-F2020/cs302-F2020-lab9-starter.git
```

You should only need to type this command once; running the command additional
times may yield an error message but will not negatively influence the state of
your Git repository. Now, you are ready to download the updates provided by the
GatorGrader maintainers by typing this command:

```
git pull download master
```

This second command can be run whenever the course instructor needs to provide
you with new source code for this assignment. However, please note that, if you
have edited the files that we updated, running the previous command may lead to
Git merge conflicts. If this happens, you may need to manually resolve them with
the help of the instructor or a student technical leader. Finally, please note
that the [Gradle plugin](https://github.com/GatorEducator/gatorgradle) for
[GatorGrader](https://github.com/GatorEducator/gatorgrader) will automatically
download the newest version of GatorGrader.

### Using GitHub Actions

This assignment uses [GitHub Actions](https://github.com/features/actions) to
automatically run [GatorGrader](https://github.com/GatorEducator/gatorgrader)
and additional checking programs every time you commit to your GitHub
repository. The checking will start as soon as you have accepted the assignment
&mdash; thus creating your own private repository &mdash; and the course
instructor and/or GitHub enables GitHub Actions on it. If you do not see either
a yellow &#9679; or a green ✔ or a red ❌ in your listing of commits, then
please ask the course instructor to see whether or not GitHub Actions was
correctly enabled.

### System Requirements

This assignment was developed to work with the following software and versions:

- Docker Desktop
- Operating Systems
  - Linux
  - MacOS
  - Windows 10 Pro
  - Windows 10 Enterprise
- Programming Language Tools
  - Gradle 6.6
  - MDL 0.5.0
  - Python 3.7 or 3.8

## Reporting Problems

If you have found a problem with this assignment's provided source code or
documentation, then you can go to the [Computer Science 302 Fall 2020 Planning
Repository](https://github.com/Allegheny-Computer-Science-302-F2020/cs302-F2020-plans)
and [raise an
issue](https://github.com/Allegheny-Computer-Science-302-F2020/cs302-F2020-plans/issues).
If you have found a problem with the [GatorGrader
tool](https://github.com/GatorEducator/gatorgrader) and the way that it checks
your assignment, then you can also [raise an
issue](https://github.com/GatorEducator/gatorgrader/issues) in that repository.
To ensure that your issue is properly resolved, please provide as many details
as is possible about the problem that you experienced. Individuals who find, and
use the appropriate GitHub issue tracker to correctly document, a mistake in any
aspect of this assignment will receive extra credit towards their grade for the
course.

## Receiving Assistance

If you are having trouble completing any part of this project, then please talk
with either the course instructor or a student technical leader during the
course session. Alternatively, you may ask questions in the Slack workspace for
this course. Finally, you can schedule a meeting during the course instructor's
office hours.
