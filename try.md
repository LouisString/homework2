

<font face = "Gabriola" size = 10 color=#0ff893b>Git Workflow</font>
===
---



<font face = "Agency FB" size = 3 >

### What's a Git workflow
</font>
<font face = "Monaco" size = 2 >

&ensp;&ensp; A _Workflow_ is a recipe or recommendation for how to accomplish work in a consistent and productive manner. A _Git workflow_ is about using `Git`, it encourages users to leverage Git effectively and consistently. 
 
&ensp;&ensp;&ensp;`Git`

&ensp;&ensp;&ensp;Anyway, workflow is not a primary theme of using `Git`, the essential problem is how to manage project isolatedly with effectiency!

&ensp;&ensp;&ensp;Let's take Sally as an example. Sally is a writer in the _Fantasy Dictionary of Biology_ association, where she and her lovely colleagues collaborate and integrate their new test-editions on their fantastic new book _Fantasy Dictionary of Biology_ these days. Of course, they take advantage of `Github` platform like below:
![There is a picture](https://github.com/LouisString/homework2/blob/master/pic1.jpg?raw=true)

With workflow's help, when writing chapter content, or composing sections, every writer work on their own `branch` at first,  then they evaluate all the writers' independent
 progresses and discuss which modifications will suit this chapter best. Thus only the best one will `merge` to the book.




<font face = "Agency FB" size = 3 >

### Types of Git workflow
</font>

&ensp;&ensp;&ensp;The shortage of tradition project management system is in the diversification and uncertainty of project flow. In this context,  workflow technology is widely discussed. In the end, it seems that not only one type of workflow exists! 



<font face = "AR ESSENCE" size = 4 >

 Centralized Workflow
</font>

&ensp;&ensp;&ensp;We know `SVN` is another Version Control Systems which uses a central repository to serve as the "single point-of-entry" for all changes to the project. Quite similarly, `Centralized Workflow`, designed for teams transitioning from `SVN`,  also adopts "single point-of-entry" concept, and has several  traits as below: 


> *  the default development branch is called `master` and all changes are committed into this branch
> * lets developers develop projects in the exact same way as they do with `SVN`.
> * lets each developer work independently of all other changes to a project
> * Access to Git’s robust branching and merging model
> * has no defined pull request or forking patterns

<font face = "AR ESSENCE" size = 4 >

 Feature Branch Workflow
</font>



&ensp;&ensp;&ensp;The core idea behind the Feature Branch Workflow is that all feature development should take place in a dedicated branch instead of the `master` branch.

 &ensp;&ensp;&ensp;This encapsulation makes it easy for multiple developers to work on a particular feature without disturbing the main codebase. It also means the `master` branch will never contain broken code, which is a huge advantage for continuous integration environments.


<font face = "Agency FB" size = 3 >

### How to use workflow?
</font>
When evaluating a workflow for your team, it's most important that you consider your team’s culture. You want the workflow to enhance the effectiveness of your team and not be a burden that limits productivity. Some things to consider when evaluating a Git workflow are:
* Does this workflow scale with team size?

* Is it easy to undo mistakes and errors with this workflow?

* Does this workflow impose any new unnecessary cognitive overhead to the team?
</font>