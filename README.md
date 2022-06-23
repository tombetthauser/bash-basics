![panda bash](https://media.tenor.com/images/ea183b7108f1ca7b4788aea8b3d7a57b/tenor.gif)

# Bash Basics

Some things I've found interesting and helpful as I've slowly learned how to make practical use of bash scripts one silly project at a time. More geared towards making clunky scripts for automating file system stuff than advanced use of the shell for workflow optimization etc.

```
⚠️ Warning: This is a work in progress and very much a reflection of a self-taught perspective!
```

### Contents:
* [what is bash](#what-is-bash)
* [check your shell](#check-your-shell)
* [comments printing & variables](#comments-printing--variables)
* [if statements](#if-statements)
* [greater than & less than](#greater-than--less-than)

---

## What is Bash?

Bash is referred to as a Unix or command line language and is an abbreviation of Bourne Again Shell. This is a reference to an earlier similar Unix shell command language (Bourne Shell) which was named after Stephen Bourne who developed it in the 1970's at Bell Labs. Bash was specifically developed as part of the Free Software Movement / GNU as a free alternative to other similar languages that were changing to for-profit models.

Bash is a syntax for communicating directly with Unix systems. Unix systems differentiate themselves from prior systems because they are built for running multiple processes concurrently. Historically on prior systems like DOS multiple processes could not be run on a single machine at the same time, and multiple users could not work on / share the same system concurrently. 

We don't have that much need for multiple users to share the same machine concurrently anymore (this was from back when computers were larger, more expensive and were often shared by multiple workers at different terminals) but we do take for granted that our computers can do more than one task at a time, and that we can open multiple shells in terminal windows, VS Code workspaces etc. We didn't always have these luxuries!

---

# The Basics

These are some very basic commands that can be run directly in your shell application (terminal etc). They can also be run as part of scripts if you save them in a file ending in sh (ie test-script.sh) and make use of them as individual lines or in more complex scenarios.

## Check Your Shell

```bash
  # confirm that you're running bash and not zsh...
  echo $0
  echo $SHELL

  # switch into bash if you're in zsh (use control+d to exit)...
  bash
  
  # switch into zsh if you're in bash (just for fun?)...
  zsh
```

📌 **Fun Fact:** You can open independent nested instances of bash inside of bash inside of zsh inside of bash etc etc.

---

## Comments Printing & Variables
```bash
  # make comments with single hash-tags like this!
  
  # print text...
  echo hello world!
  
  # declare variables (cant use spaces)...
  a=42
  b=hello
  c='hello world!'
  
  # check variables using echo and the special $ charactor...
  echo $a
  echo $b
  echo $c
  
  # re-assign and exising variable...
  a=2501
  
  # echo environment variables (case-sensitive)...
  echo $USER
  echo $SHELL
  
  # check all environment variables...
  export
```

---

# Conditionals and Loops

These can be written directly in the shell but are probably best written in a script file and then run. Make a file ending in sh (my-script.sh), write any valid bash syntax, save it, exit your editor and then run the file by typing ```$ bash my-script.sh``` which will run all the files commands.

## If Statements
```bash
  # some basic conditionals...

  if [ 'something' ]
  then
    echo 'a string is truthy!'
  fi

  if []
  then
    echo 'this wont print!'
  fi

  if [ 1 = 1 ]
  then
    echo 'one equals one!'
  fi
  
  if [ 1 = 42 ]
  then
    echo 'this wont print!'
  fi
  
  if [ 'cat' = 'cat' ]
  then
    echo 'cat equals cat!'
  fi
  
  if [ 1 = 1 ]
  then echo 'one line then command!'
  fi
  
  if [ 1 = 1 ]; then echo 'one line conditional!'; fi

  # quotes are not needed if spaces aren't in variables...
  a="cat"
  b="cat"
  if [ $b = $a ]
  then
    echo 'true!'
  fi

  # quotes are needed if spaces aren't in variables...
  a="my cat"
  b="my cat"
  if [ "$b" = "$a" ]
  then
    echo 'true!'
  fi

  # double equals is just alternative syntax...
  if [ 1 == 1 ]
  then
    echo 'double equals works!'
  fi
  
  # all equals comparisons are loose...
  if [ "1" == 1 ]; then echo 'true!'; fi
  if [ "1" = 1 ]; then echo 'also true!'; fi
  
```

---

## Greater Than & Less Than
```bash
  if [ 1 -gt 0 ]
  then
    echo '1 is greater than 0!'
  fi
  
  if [ 0 -gt 1 ]
  then
    echo 'this wont print!'
  fi
  
  if [ 0 -lt 1 ]
  then
    echo '0 is less than 1!'
  fi
  
  if [ 1 -eq 1 ]
  then
    echo 'we can use -eq instead of "="'
  fi
  
  # note that quotes don't matter...
  if [ "1" -gt 0 ]; then echo 'true!'; fi
  if [ "1" -eq 1 ]; then echo 'also true!'; fi
  if [ "1" -lt 0 ]; then echo 'not true!'; fi

```
