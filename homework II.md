

<font face = "Gabriola" size = 10 color=#0ff893b>Git Workflow</font>
===
---



<font face = "Agency FB" size = 5 >

### What's a Git workflow
</font>
<font face = "Monaco" size = 2 >

&ensp;&ensp; A _Workflow_ is a recipe or recommendation for how to accomplish work in a consistent and productive manner. A _Git workflow_ is about using `Git`, it encourages users to leverage Git effectively and consistently. 
 
&ensp;&ensp;&ensp;`Git`

&ensp;&ensp;&ensp;Anyway, workflow is not a primary theme of using `Git`, the essential problem is how to manage project isolatedly with effectiency!

&ensp;&ensp;&ensp;Let's take Sally as an example. Sally is a writer in the _Fantasy Dictionary of Biology_ association, where she and her lovely colleagues collaborate and integrate their new test-editions on their fantastic new book _Fantasy Dictionary of Biology_ these days. Of course, they take advantage of `Github` platform like below:
![There is a picture](https://github.com/LouisString/homework2/blob/master/pic1.jpg?raw=true)


With workflow's help, when writing chapter content, or composing sections, every writer work on their own `branch` at first,  then they evaluate all the writers' independent 
 progresses,  then discuss which modifications will suit this chapter best and approve the pushed commits. Thus only the best one will "merge" to the book.

![](https://github.com/LouisString/homework2/blob/master/pic2.jpg?raw=true)


<font face = "Agency FB" size = 5 >

### Types of Git workflow
</font>

&ensp;&ensp;&ensp;The shortage of tradition project management system is in the diversification and uncertainty of project flow. In this context,  workflow technology is widely discussed. In the end, it seems that not only one type of workflow exists! 


<br/><br/>
<font face = "AR ESSENCE" size = 5 >

 Centralized Workflow
</font>

![](https://github.com/LouisString/homework2/blob/master/pic3.png?raw=true)

&ensp;&ensp;&ensp;We know `SVN` is another Version Control Systems which uses a central repository to serve as the "single point-of-entry" for all changes to the project. Quite similarly, Centralized Workflow, designed for teams transitioning from `SVN`,  also adopts "single point-of-entry" concept, and has several  traits as below: 


> *  the default development branch is called `master` and all changes are committed into this branch
> * lets developers develop projects in the exact same way as they do with `SVN`.
> * lets each developer work independently of all other changes to a project
> * Access to Git’s robust branching and merging model
> * has no defined pull request or forking patterns

&ensp;&ensp;&ensp;So a Centralized Workflow is generally better suited for teams **migrating from SVN to Git and smaller size teams!**

<font face = "Bradley Hand ITC" size = 4 >

### How to use it?
</font>

![](https://github.com/LouisString/homework2/blob/master/pic4.png?raw=true)

&ensp;&ensp;&ensp;To publish changes to the official project, developers "push" their local master branch to the central repository. This is the equivalent of `SVN` commit, except that it adds all of the local commits that aren’t already in the central master branch.

&ensp;&ensp;&ensp;Basicly:
>* create the central repository on a server
>* each developer creates a local copy of the entire project
>* push the new committed changes to the central repository

 &ensp;&ensp;&ensp;If a developer’s local commits diverge from the central repository, `Git` will refuse to push their changes because this would overwrite official commits. So its commit history comes to a divergence:

 ![](https://github.com/LouisString/homework2/blob/master/pic5.png?raw=true)

&ensp;&ensp;&ensp;Before the developer can publish their feature, they need to fetch the updated central commits and rebase their changes on top of them! Git makes it very easy for new developers to manage their own merges, or to abort the entire rebase and try again.

&ensp;&ensp;&ensp;Remember:

>* There is no one-size-fits-all Git workflow
>* A workflow should be simple and enhance the productivity of your team
>* Your business requirements should help shape your Git workflow


&ensp;&ensp;&ensp;Here is one detailed process for examble:

>**John works on his feature**

![](https://github.com/LouisString/homework2/blob/master/pic19.png?raw=true)

>**Marry works on his feature**

![](https://github.com/LouisString/homework2/blob/master/pic20.png?raw=true)

>**John publishes his feature successfully**

![](https://github.com/LouisString/homework2/blob/master/pic21.png?raw=true)

>**Mary tries to publish her feature but her local history has diverged from the central repository**

![](https://github.com/LouisString/homework2/blob/master/pic22.png?raw=true)

>**Mary rebases on top of John’s commit(s)**

![](https://github.com/LouisString/homework2/blob/master/pic23.png?raw=true)

>**synchronise upstream commit history with Marry's local commits**

![](https://github.com/LouisString/homework2/blob/master/pic24.png?raw=true)

>**Mary resolves a merge conflict**

![](https://github.com/LouisString/homework2/blob/master/pic25.png?raw=true)


![](https://github.com/LouisString/homework2/blob/master/pic26.png?raw=true)

>**Mary successfully publishes her feature!**

![](https://github.com/LouisString/homework2/blob/master/pic27.png?raw=true)

<br/><br/><br/><br/>
<font face = "AR ESSENCE" size = 5 >

 Feature Branch Workflow
</font>



&ensp;&ensp;&ensp;The Git Feature Branch Workflow is a composable workflow that can be leveraged by other high-level Git workflows.  The core idea behind it is that **all feature development should take place in a dedicated branch** instead of the `master` branch.

&ensp;&ensp;&ensp;It has following advantages:


 >* focused on branching patterns
>* can be leveraged by other repo oriented workflows
> * promotes collaboration with team members through pull requests and merge reviews

&ensp;&ensp;&ensp;Once someone completes a feature, they don’t immediately merge it into master. Instead, they push the feature branch to the central server and file a pull request asking to merge their additions into master.

&ensp;&ensp;&ensp;This gives other developers an opportunity to review the changes before they become a part of the main codebase.

&ensp;&ensp;&ensp;Here are several pictures in order to show procedures above:



<font face = "Bradley Hand ITC" size = 4 >

### How to use it?
</font>

&ensp;&ensp;&ensp;Basicly:

>* start with the master branch
>* create a new branch every time on a new feature.
>* update, add, commit, and push changes; work on the feature and make commits 
>* push the feature branch up to the central repository
>* resolve feedback,  resolve merge conflicts and merge your pull request 

&ensp;&ensp;&ensp;Once a pull request is accepted, the actual act of publishing a feature is much the same as in the Centralized Workflow!

&ensp;&ensp;&ensp;Also, let's see an example:

>**Mary begins a new feature**

![](https://github.com/LouisString/homework2/blob/master/pic13.png?raw=true)

>**Mary push her feature branch up to the central repository and goes to lunch**

![](https://github.com/LouisString/homework2/blob/master/pic14.png?raw=true)

>**Mary finishes her feature**

![](https://github.com/LouisString/homework2/blob/master/pic15.png?raw=true)

>**Bill receives the pull request**

![](https://github.com/LouisString/homework2/blob/master/pic16.png?raw=true)

>**Mary makes the changes, and Bill could pull marys-feature into his local repository**

![](https://github.com/LouisString/homework2/blob/master/pic17.png?raw=true)

>**Mary publishes her feature**

![](https://github.com/LouisString/homework2/blob/master/pic18.png?raw=true)



<br/><br/><br/><br/>
<font face = "AR ESSENCE" size = 5 >

 Gitflow Workflow
</font>

&ensp;&ensp;&ensp;Gitflow Workflow defines a strict branching model designed around the project release. This provides a robust framework for managing larger projects.  

&ensp;&ensp;&ensp;Gitflow is just an abstract idea of a Git workflow. However, it is **ideally suited for projects that have a scheduled release cycle.** This workflow doesn’t add any new concepts or commands beyond what’s required for the Feature Branch Workflow. Instead, it assigns very specific roles to different branches and defines how and when they should interact! 



&ensp;&ensp;&ensp;Compared to Feature Branch Workflow we talked above:
>* it uses individual branches for preparing, maintaining, and recording releases.
>* it dictates what kind of branches to set up and how to merge them together.
>* it is more involved with extension command like<pre><code>git flow init</code></pre>
>* it has 2 main branches: The `master` branch stores the official release history, and the `develop` branch serves as an integration branch for features.


<font face = "Bradley Hand ITC" size = 4 >

### How it works?
</font>

![](https://github.com/LouisString/homework2/blob/master/pic7.png?raw=true)

&ensp;&ensp;&ensp;The default master is complemented with a develop branch, this branch will contain the complete history of the project, whereas master will contain an abridged version.
Instead of branching off of master, feature branches use develop as their parent branch.

![](https://github.com/LouisString/homework2/blob/master/pic8.png?raw=true)

&ensp;&ensp;&ensp;Each new feature should reside in its own `develop` branch. When a feature is complete, it gets merged back into develop.


![](https://github.com/LouisString/homework2/blob/master/pic9.png?raw=true)


&ensp;&ensp;&ensp;Once develop has acquired enough features for a release, fork a release branch off of develop.
&ensp;&ensp;&ensp;Creating this branch starts the next release cycle, so no new features can be added after this point -- only bug fixes!

![](https://github.com/LouisString/homework2/blob/master/pic10.png?raw=true)

&ensp;&ensp;&ensp;Now we've got to Maintain the production. Hotfix branches are a lot like release branches and feature branches except they're based on master instead of develop. As soon as the fix is complete, it should be merged into both master and develop (or the current release branch), and master should be tagged with an updated version number.



&ensp;&ensp;&ensp;Using a dedicated branch to prepare releases makes it possible for one team to polish the current release while another team continues working on features for the next release. It also creates well-defined phases of development. 

&ensp;&ensp;&ensp;So, we see the overall flow of Gitflow is:
>* A develop branch is created from master
>* A release branch is created from develop
>* Feature branches are created from develop
>* When a feature is complete it is merged into the release branch
>* When the release branch is done it is merged into develop and master
>* If an issue in master is detected a hotfix branch is created from master
>* Once the hotfix is complete it is merged to both develop and master
  
<br/><br/><br/><br/>
<font face = "AR ESSENCE" size = 5 >

 Forking Workflow
</font>

&ensp;&ensp;&ensp;The Forking Workflow is fundamentally different than other popular Git workflows. It gives every developer their own **server-side repository**. 

&ensp;&ensp;&ensp;The main advantage of the Forking Workflow is: developers push to their own server-side repositories, and only the project maintainer can push to the official repository. This means ONLY maintainer have write access to the official codebase.

&ensp;&ensp;&ensp;Thus, the Forking Workflow typically follows a branching model based on the Gitflow Workflow. It is an **ideal workflow for open source projects**.


<font face = "Bradley Hand ITC" size = 4 >

### How it works?
</font>

![](https://github.com/LouisString/homework2/blob/master/pic11.png?raw=true)

&ensp;&ensp;&ensp;When a new developer wants to start working on the project, they can not directly clone the official repository anymore. Instead, they fork the official repository to create a copy of it on the server. This new copy serves as their personal public repository.

&ensp;&ensp;&ensp;When they're ready to publish a local commit, they push the commit to their own public repository. Then, they file a pull request with the main repository, which lets the project maintainer know that an update is ready to be integrated.

&ensp;&ensp;&ensp;Here is the detailed procedures:

>* A developer 'forks' an 'official' server-side repository. This creates their own server-side copy.
>* The new server-side copy is cloned to their local system.
>* A Git remote path for the 'official' repository is added to the local clone.
>* A new local feature branch is created.
>* The developer makes changes on the new branch.
>* The branch gets pushed to the developer's own server-side copy.
>* The developer opens a pull request from the new branch to the 'official' repository.
>* The pull request gets approved for merge and is merged into the original server-side repository


&ensp;&ensp;&ensp;To integrate the feature into the official codebase, the maintainer pulls the contributor’s changes into their local repository, merges it into his local master branch, then pushes the master branch to the official repository on the server.

&ensp;&ensp;&ensp;The contribution is now part of the project, and other developers should pull from the official repository to synchronize their local repositories.

&ensp;&ensp;&ensp;Here is a family picture:
![](https://github.com/LouisString/homework2/blob/master/pic12.png?raw=true)

&ensp;&ensp;&ensp;A high-level example of a Forking Workflow is:
 
>* You want to contribute to an open source library hosted at bitbucket.org/userA/open-project
>* Using Bitbucket you create a fork of the repo to bitbucket.org/YourName/open-project
>* On your local system you execute git clone on https://bitbucket.org/YourName/open-project to get a local copy of the repo
>* You create a new feature branch in your local repo
>* Work is done to complete the new feature and git commit is executed to save the changes
>* You then push the new feature branch to your remote forked repo
>* Using Bitbucket you open up a pull request for the new branch against the original repo at bitbucket.org/userA/open-project

&ensp;&ensp;&ensp;Thanks for reading!

</font>