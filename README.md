### What is GIT ?

```
Git is a version control system used by almost all the organizations to version control your development 

``` 

### How can control parallel development and how multiple developers can contribute, develop code parallely?
```
Git branches is the only solution for parallel development and parallel contribution
```

### What is a Git Branch ?

```
A branch is a version of your repository, or in other words, an independent line of development. A 
repository can contain multiple branches, which means there are multiple versions of the repository.

Among all, main / master branch is something which you should always a checkout to create a new /feature 
branch
```

### Git Branch Naming Sttagegy

```
Branch Naming will be based on your organization.

Either you will work on developing,
    a) a feature 
    b) a hotfix
    c) a bug

So, majority of the times, your branch names should be the following way

    a) feature/story-number 
    b) hotfix/ story-number 
    c) bug/story-number
    d) story-number

```

### Common GIT Commands

```
$ git branch                                       // Shows you list of branches and your current branch
$ git branch brancName                             // Creates a branch from the main branch 
$ git checkout branchName                          // Switches to the created branch
$ git checkout -b branchName                       // Creates a new branch from main branch as source and 
swithes to the created branch
$ git push origin remoteBranchName                 // Pushes the changes to the remote branch; If branch 
doesn't exist on remote git, it creates by the same push   

Whenever you push any changes and if they look good and stable on main branch, then you will raise/create
a create a Git Tag.

Git Tag : Creating a name to a commit, which can referenced later and using that we can make the software.


Git and Linux are like oceans, infinite things are there to learn. Both of them are created by the same 
person : Linux Torvalds
```
### Practice
Open gitbash
Change to directoty to be tagged
$ cd sudedevops/ansible
List the tags already present
$ git tag -l 
Choose the release number and tag them locally
$ git tag 0.0.2
Push them to repo
$ git push --tags
View the list of tags to confirm
$ git tag -l

Finding the latest release number,incrementing to next patch/service release number, and tagging is automated.
$ bash sudedevops/ansible/auto-tag.sh

Delete the tag locally
$ git tag -d 0.0.3
Delete the tag at remote repo
$ git push --delete origin 0.0.3

