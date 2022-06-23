![panda bash](https://media.tenor.com/images/ea183b7108f1ca7b4788aea8b3d7a57b/tenor.gif)

# Bash Basics

Some things I've found interesting and helpful as I've slowly learned how to make practical use of bash scripts one silly project at a time. More geared towards making automation scripts than advanced use of the shell for workflow optimization etc. An imperfect reflection of my imperfect self-teaching process.

```
⚠️ Warning: This is a work in progress and very much a reflection of a self-taught perspective!
```

### Contents:
* [What is Bash?](#what-is-bash)
* [Simple Commands](#simple-commands)

---

## What is Bash?

Bash is referred to as a Unix or command line language and is an abbreviation of Bourne Again Shell. This is a reference to an earlier similar Unix shell command language (Bourne Shell) which was named after Stephen Bourne who developed it in the 1970's at Bell Labs. Bash was specifically developed as part of the Free Software Movement / GNU movement as a free alternative to other similar languages that were changing to for-profit endeavors.

Bash is a syntax for communicating directly with Unix systems. Unix systems differentiate themselves from prior systems because they are built for running multiple processes concurrently. Historically on prior systems like DOS multiple processes could not be run on a single machine at the same time, and multiple users could not work on / share the same system concurrently. 

We don't have that much need for multiple users to share the same machine concurrently anymore (this was from back when computers were larger, more expensive and were often shared by multiple workers at different terminals) but we do take for granted that our computers can do more than one task at a time, and that we can open multiple shells in terminal windows, VS Code workspaces etc. We didn't always have these luxuries!

---

## Simple Commands

These are some very basic commands that can be run directly in your shell application (terminal etc). They can also be run as part of scripts if you save them in a file ending in sh (ie test-script.sh) and make use of them as individual lines or in more complex scenarios.

Confirm that you're running bash and not zsh...
```bash
  echo $0
```

Switch into bash if you're working in zsh (use control+d to exit)...
```bash
  bash
```

Switch into zsh if you're working in bash (just for fun?)...
```bash
  bash
```

📌 **Fun Fact:** You can open independent nested instances of bash inside of bash inside of zsh inside of bash etc etc.

Make comments, echo / print stuff, declare variables and check them with echo...
```bash
  # make comments with single hash-tags like this!
  
  # print text...
  echo hello world!
  
  # declare variables (cant use spaces)...
  a=10
  b=hello
  c='hello world!'
  
  # check variables using echo and the special $ charactor...
  echo $a
  echo $b
  echo $c
  
  # echo environment variables (case-sensitive)...
  echo $USER
  echo $LANG
  echo $PATH
  
  # check all environment variables...
  export
```

