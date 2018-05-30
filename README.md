Overview
--------
`kickstartR` is a set of functions that are designed to make it easy to speed through the tedious startup stage of any new project. `kickstartR` is a package in development. There are 2 functions currently included in the package (_highlighted below_), but we plan on adding more as we find time outside our busy lives.
&nbsp;  

Installation
------------
 The development version of kickstartR can be downloaded from GitHub using the `devtools` package.

```
# install.packages("devtools")
devtools::install_github("mgolafshar/kickstartR")
```

Functions
------------  

### The `create.proj()` function
   
You've been handed an exciting project and are eager to dig in, but, before you can start writing code and exploring the data, you need to set up your project directories. The `create.proj()` function does it it for you. Simply feed it a path, project name and any number of subfolders, then get to work.

#### _Example:_
Create a project called "Project_x" on your desktop with 3 subfolders called "Mulder", "Scully" and "The_Truth", plus a blank README.md file:
```
create.proj(path = "~/Desktop", 
            parent = "Project_x", 
            sub = c("Mulder", "Scully", "The_Truth"), 
            doctype = "md")
```
&nbsp;  

### The `packages()` function  
  
`packages()` is a function that simplifies the process of loading multiple libraries. Feed the `packages()` function a list of packages, and it will load them all for you (_including downloading them from CRAN if necessary_).

#### _Example:_
```
# Feed it a list of packages
packages(c("tidyverse", "arsenal", "survival"))

# Or better yet...feed it a space-separated string
packages("tidyverse arsenal survival")

```

