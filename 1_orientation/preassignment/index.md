---
title: "Preassignment: Days 1 and 2"
---

This is a **long** preassignment that involves lots of software installation and testing. Please leave a total of at least **2 hours** to complete this preassignment. That may seem like a long time, but once you've done it you'll have a powerful suite of software that you can use through your career at MIT and beyond. 

# 1. Version Control: Git and GitHub

How can we manage complex, code-based workflows? How can we reliably share code between collaborators without syncing issues? How can we track multiple versions of scripts without going crazy? There are multiple solutions to these problems, but *version control* with git is by far the most common. 

<!-- ## Install git

Get started by installing Git. You can follow the relevant instructions for your operating system [here](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git). For Windows 10 users, we suggest installing and interacting with git either via the [Windows Subsystem for Linux](https://docs.microsoft.com/en-us/windows/wsl/install-win10) or via the [GitHub Desktop Client](https://desktop.github.com).
 -->
## Make an Account on GitHub.com

[GitHub](https://github.com/) is a hosting service for git that makes it easy to share your code. 

Sign up for an account -- remember to keep track of your username and password. Feel free to enter information about yourself and optionally a profile picture. 

## Install GitHub Desktop

Download GitHub Desktop [here](https://desktop.github.com), and follow the installation directions. 

During setup, you will be prompted to enter your username and password from GitHub. 

*If you have used git previously and prefer to interact with it via the command line, that's fine. However, we won't be giving command line instructions and won't help you if you get stuck by doing something silly.* 

## Test Your Installation

As a very basic use case, we are going to use git and GitHub to access the course materials. The course materials live in a repository ("repo") on GitHub. There are three main steps: 

1. *Fork* the repo on GitHub. This creates a copy of the class repo under your own account. Changes you make here won't be reflected in the original repo -- think of it as your playground. 
2. *Clone* the forked repo from GitHub to your computer. Here's where you'll interact with the files. 
3. After changing files, you can *push* your changes back up to GitHub. Let's see how this all works. 

**Fork the Repo**

Navigate to [`https://github.com/PhilChodrow/mban_orientation`](https://github.com/PhilChodrow/mban_orientation). Make sure you are signed in. Click the "Fork" button.

![](figs/fork.png)

You now have a copy of the mban_orientation repo under your own user account. 

**Clone the Repo**

Now go to GitHub Desktop. Choose "Clone Repository," and click the URL tab.  In the first field, enter `your_name/mban_orientation`. In the second field, enter the location on your computer where you would like to place the materials. Your desktop is fine. 

![](figs/clone.png)

Take a moment to check that the folder containing some files has appeared in the specified location on your computer. 

**Edit Some Files**

Open the file `1_orientation/1_git/README.md` in a text editor. Replace the first line of text with "# [your_name or GitHub username]". 

**Push Your Changes**

Once you have made your changes in the file, check back on GitHub Desktop. The client has noticed that you have changed this file, and even gives a visual description of what change you made. 

![](figs/commit_push.png)

In the "Summary" field, write "git preassignment." Then, click "Commit to master" and then "Push origin." To check that this worked: 

1. Navigate back to your fork of the repository on GitHub.com in your browser. 
2. Click through `1_orientation/1_git`. The file README.md is rendered at the bottom. It should have your name on it. 

If that's what you see, congratulations! You are up and running with git and GitHub, and are ready to move on to the next phase of the preassignment. 

**If You Encounter Problems**

1. If you receive an error message, Google it. 
2. If you tried that, write an email to `pchodrow@mit.edu` describing the problem in as much detail as possible, preferably including screenshots.  


# 2. Data Analysis: R and RStudio

## Install R and RStudio

**We are assuming that you have recent versions of R and RStudio installed.** In particular, you need R version 3.5.1 and RStudio 1.1.456. For this reason, we **strongly recommend** that you download and install both R and RStudio, even if both are already on your laptop. 
 
1. **Install R**: Navigate to [`https://cran.cnr.berkeley.edu/`](https://cran.cnr.berkeley.edu/) and follow the instructions for your operating system. 
2. **Download RStudio**: Navigate to [`https://www.rstudio.com/products/rstudio/download/`](https://www.rstudio.com/products/rstudio/download/) and download RStudio Desktop with an Open Source License. 
3. **Test Your Installation**: Open RStudio and type 1+2 into the Console window, and press "Enter." If you see the expected result, you are ready to move on. 

## Install Packages

In the RStudio console, type 
```R
pkgs <- c('tidyverse', 'knitr', 'flexdashboard', 'nycflights13', 'ggmap')
install.packages(pkgs)
```

If you encounter any error messages that you are unable to handle, please email Phil at `pchodrow@mit.edu`. 

## Test Packages

In the folder on your desktop from which you downloaded the repo, open the file `1_orientation/2_data_science/code/dashboard.rmd`. It will open in RStudio. Click the "Knit" button at the top of the source editor, or press `cmd + shift + k` (`ctrl + shift + k` on Windows). The "Knit" button is the one circled in [this image](http://cinf401.artifice.cc/images/workflow-25.png). You will need to be connected to the internet in order for this to work. 

After a few moments, RStudio should pop up with a new window containing a dashboard that looks like [this](https://philchodrow.github.io/mban_orientation/1_orientation/2_data_science/code/dashboard.html).  If your output matches the example, congratulations! You are up and running with R and RStudio. Move on to the next step. 

**If You Encounter Problems**

1. If you receive an error message, Google it. 
2. If you tried that, write an email to `pchodrow@mit.edu` describing the problem in as much detail as possible, preferably including screenshots.  


# 3. Optimization: Julia and JuMP

**Please try to complete all the steps below before the first day of class.** We will only be using Julia and Gurobi on the second day, but we have very limited time in class and we will not be able to help you with installation problems during the teaching time. If you have difficulties with the installations below, please email `mban-orientation-2019@mit.edu` and include as much information as possible so that we can assist you.

Note that you will need to be connected to the MIT network to activate one of these installations, but most of the other steps can be completed from any location. 

## Install Julia

Julia is programming language developed at MIT. To install Julia, go to [`https://julialang.org/downloads/`](https://julialang.org/downloads/) and download the appropriate version for your operating system. See [`here`](https://julialang.org/downloads/platform.html) for more detailed instructions.
We will assume that everyone has installed the most recent version of Julia (v1.1). If you have an older version installed, we recommend that you install the newer version as well.

To confirm that Julia is installed, open a Julia window by clicking on the Julia icon in your applications menu (note: mac users should make sure Julia is copied into their applications folder). You should see a prompt at the bottom of the new window that looks like this:

```julia
julia>
```

Type 1+1 after the prompt and press enter/return.
```julia
julia> 1+1
2
```
If you see the response above, Julia is working!

## Install JuMP

JuMP is a Julia package that we will use to create optimization models in class. To install this package, run the following lines in the Julia window:
```julia
julia> using Pkg
julia> Pkg.add("JuMP")
```

This might take quite a while to finish, so don’t worry if it looks like nothing is happening in the Julia window. You will know that the process is complete when you see the command prompt (julia>) appear at the bottom of your screen.

To test if the package is installed correctly, run the following commands
```julia
julia> using JuMP
julia> m = Model()
```
You should see the output below

```julia
A JuMP Model
Feasibility problem with:
Variables: 0
```


## Install Gurobi

Gurobi is a commercial optimization solver that we will use to solve optimization problems in class. Here are the basic steps that you will need to follow to install Gurobi:

1. Make a Gurobi account [`here`](https://www.gurobi.com/registration-general-reg/) using your @mit.edu email address (select the Academic option, not the commercial option).
2. Download the Gurobi Optimizer software [`here`](https://www.gurobi.com/downloads/) and install.
3. Create and download an Academic License to use the software [`here`](https://www.gurobi.com/downloads/end-user-license-agreement-academic/).
4. Use the license file to activate the Gurobi software that you installed. Follow the instructions on the license page to run the grbgetkey command. **Note that you must be connected to the MIT SECURE network to do this.** If you are not on campus, please move on to the next section (IJulia) and come back to this step later.

A summary of the Gurobi installation/activation process is available [`here`](https://www.gurobi.com/academia/academic-program-and-licenses/) and detailed installation instructions are available [`here`](https://www.gurobi.com/documentation/quickstart.html). If you get stuck trying to follow these instructions, please email `mban-orientation-2019@mit.edu` for assistance.

After installing Gurobi, we need to add a Julia package called "Gurobi" that allows Julia to communicate with the Gurobi software. Run the following lines in your Julia window:
```julia
julia> using Pkg
julia> Pkg.add("Gurobi")
```
If you see error messages during this installation, it could be because you did not install/activate Gurobi properly. Please read through the "Installation" information [`here`](https://github.com/JuliaOpt/Gurobi.jl) and see the instructions for setting the GUROBI_HOME environment variable.

If the Gurobi package is successfully installed in Julia, run the following lines:
```julia
julia> using JuMP, Gurobi
julia> model = Model(with_optimizer(Gurobi.Optimizer, Presolve=0, OutputFlag=0))
```

You should see this output:

```julia
A JuMP Model
Feasibility problem with:
Variables: 0
Model mode: AUTOMATIC
CachingOptimizer state: EMPTY_OPTIMIZER
Solver name: Gurobi
```

## Install IJulia and Jupyter

Jupyter is a free, open-source program that will allow us to write and run Julia code in a web browser (instead of typing everything into the command line). IJulia is a Julia package that allows Julia to communicate with the Jupyter software. Instead of installing Jupyter on its own, we can use the IJulia package to install it within Julia.

Run the following lines in a Julia window:

```julia
julia> using Pkg
julia> Pkg.add("IJulia")
julia> using IJulia
```

These lines download and install the IJulia package. 
Now, we will try to open a Jupyter notebook. If Jupyter is not installed, Julia will ask if we want to install it now. Run the following line, and then press enter/return or y to install Jupyter:
```julia
julia> notebook()
install Jupyter via Conda, y/n? [y]: 
```

If this is successful, a Jupyter tab will open in the default browser on your computer. Click “New” in the top right corner to make a new notebook (if a menu appears, select Julia 1.1). A new tab will open with a blank Jupyter notebook.

## Final Check

Once you have completed all the steps above, copy and paste the following code into a new Jupyter notebook (next to the "In []:"" prompt)

```julia
using JuMP, Gurobi
model = Model(with_optimizer(Gurobi.Optimizer, Presolve=0, OutputFlag=0))
@variable(model,x>=0)
@objective(model, Min, x)
optimize!(model)
print("The answer is ",JuMP.value(x))
```

Now, click the "Run" button to run this code. You should see this output below:

```julia
The answer is 0.0
```

If you see this output, everything is working correctly. If you see errors, one of the steps above may be incomplete. If you don't see any output, make sure that you have selected the notebook cell where you paste the code and try to run it again. 

**If you've made it this far, congratulations!** You now possess a powerful set of tools for analyzing data, solving optimization problems, and collaborating on code. You're ready to go!  



