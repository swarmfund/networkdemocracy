# README #

### What is this repository for? ###
This repo contains useful macros for people working with categorical quantum mechanics and related fields.


### How do I download these macros? ###
**I just want to download the macros. The project I'm working on is not on GIT.**

From a terminal window, just navigate to your project main folder and give


```
#!bash

git clone git@bitbucket.org:Nigredo/quantum-latex-macros.git
```


A folder named 'quantum-latex-macros' will appear in your main folder.

**I want to download the macros, but the project I'm working on is already on GIT.**

Just navigate to your project main folder and give

```
#!bash
git subtree add --prefix=quantum-latex-macros/ git@bitbucket.org:Nigredo/quantum-latex-macros.git master --squash

```
The *--squash* command omits all the commit history of these macros, that would just make your project balloon in size with no reason. If you want to copy the whole commit history in your project just leave the *--squash* command out.

A folder named *quantum-latex-macros* will appear in your main folder. This will not interfere with your GIT project, and you will be able to push/pull/commit as you always do. The macros will be just like any other folder in your project and you will be able to modify them as you wish. In particular, the macros will already be there when anyone clones your project, so your colleagues won't have to do anything.

### How do I get set up? ###
Just put this in your main tex file:

```
#!latex

\newcommand{\yourpath}{quantum-latex-macros/}
\usepackage{import}
\subimport{\yourpath/}{packages}
\subimport{\yourpath/}{macros}
\subimport{\yourpath/}{tikzstyles}
```


If you dowloaded the macros in a different folder/path than the one I suggested before you just have to edit the following line


```
#!latex

\newcommand{\yourpath}{quantum-latex-macros/}
```


replacing *quantum-latex-macros* with your folder path.

### Updating the macros ### 
I do not suggest to update these macros within a project. Some command names may have changed and you could have to rewrite part of your stuff. Anyway, if you to proceed:

**I just downloaded the macros. The project I'm working on is not on GIT.**

Just navigate to the macros folder and give 

```
#!bash

git pull
```

within it.

**I downloaded the macros in my GIT project.**

The command in this case is 


```
#!bash

git subtree pull --prefix=quantum-latex-macros/ git@bitbucket.org:Nigredo/quantum-latex-macros.git master

```

to be given anywhere in your project folder. You may have to change *quantum-latex-macros/* to something else if you cloned the macros in some other path.

### Contribution guidelines ###

If you want to contribute to this project just mail me (see last section) and I'll give you writing rights to it. If you have writing privilege to this repo keep reading, otherwise ignore this section.

If you just cloned the macros into a clean folder you can push and commit as you normally do in GIT. 

If you want to do a change on the fly while working on another project then the *commit* command stays the same (GIT understands when a commit applies to the macros and when it does not). To push, the useful command is


```
#!bash

git subtree push --prefix=quantum-latex-macros/ git@bitbucket.org:Nigredo/quantum-latex-macros.git master
```

### Automatizing everything ###
If you really like these macros you may want to create an alias to make stuff easier. On linux, just add this to your *~/.bashrc* file:


```
#!bash

alias Latexaddmacros="git subtree add --prefix=quantum-latex-macros/ git@bitbucket.org:Nigredo/quantum-latex-macros.git master"

alias Latexpullmacros="git subtree pull --prefix=quantum-latex-macros/ git@bitbucket.org:Nigredo/quantum-latex-macros.git master"
```

Now you will just have to give *Latexaddmacros* and *Latexpullmacros* within your GIT project folder to add or update the macros, respectively.

### Who do I talk to? ###

fabrizio.genovese@cs.ox.ac.uk