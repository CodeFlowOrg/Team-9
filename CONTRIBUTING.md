# Contribution Guidelines
> **Note**: Start working only after you have been assigned the task. Pull requests made to unassigned tasks will be rejected.
- If you create a new issue, **wait for the maintainers to assign** it to you as well.
- **Do not** overwrite contributions done by other people.


# Contribution Guide
*Make sure you have a GitHub account. In case you don't have one, you can create your account by visiting https://github.com/ and clicking on ``Sign up`` option at the top right corner.*

### 1. Register yourself for Hacktoberfest
Link to register: https://hacktoberfest.digitalocean.com/ \
Click on "Start Hacking" and add your GitHub account.



### 2. Star and Fork this Repository
You can star and fork this repository on GitHub by navigating at the top of this repository.

![Fork this repository](https://camo.githubusercontent.com/b22b37874052e69f2e83743b5763440aec7af332e6ea51df6b86652a343d8b6e/68747470733a2f2f68656c702e6769746875622e636f6d2f6173736574732f696d616765732f68656c702f7265706f7369746f72792f666f726b5f627574746f6e2e6a7067)

After forking, you will see two repositories with the same name 'dsc-hacktoberfest-2021'. 
  - CodeFlow201/Team-9
  - your-username/Team-9

You can make changes directly to **your** repository i.e. `your-username/Team-9` but you cannot make changes to **this** repository directly. You can contribute here by submitting your changes as `pull requests`.


### 3. Clone the Repository

To make a local copy of the forked repository, let’s first open up a terminal window.

We’ll use the `git clone`  command along with the URL that points to your fork of the repository.

This URL will consist of your username and it will end with `.git`. The URL will look like this: https://github.com/your-username/Team-9.git

You can alternatively copy the URL by clicking on the green “Code” button from your repository page. Once you click the button, you’ll be able to copy the URL by clicking the binder button next to the URL
![Copy the URL using the Code button](https://camo.githubusercontent.com/7874a18f4d58d18ef485cdae8acae5e0591f02c7ed955bb7ad9d111153a20da8/68747470733a2f2f646f63732e6769746875622e636f6d2f6173736574732f696d616765732f68656c702f7265706f7369746f72792f636f64652d627574746f6e2e706e67)

Once we have the URL, we’re ready to clone the repository. To do this, we’ll combine the git clone command with the repository URL from the command line in a terminal window:

````bash
$ git clone https://github.com/your-username/Team-9.git
````


### 4. Create a New Branch

To create your branch, from your terminal window, change your directory so that you are working in the directory of the repository. Be sure to use the actual name of the repository to switch into that directory.

````bash
$ cd Team-9/
````

Now, we’ll create a new branch with the git branch command. Make sure you name it descriptively so that others working on the project understand what you are working on.
````bash
$ git branch new-branch
````


Now that our new branch is created, we will switch over to it using the git checkout command:
````bash
$ git checkout new-branch
Switched to branch 'new-branch'
````

At this point, you can now modify existing files or add new files to the project on your branch.

#### Make Changes Locally

Once you have modified existing files or added new files to the project, you can add them to your local repository, which you can do with the git add command. Let’s add the -A flag to add all changes that we have made:

````bash
$ git add -A
````
or
````bash
$ git add . 
````

Next, we’ll want to record the changes that we made to the repository with the git commit command.

*The commit message is an important aspect of your code contribution; it helps the other contributors fully understand the change you have made, why you made it, and how significant it is. Additionally, commit messages to provide a historical record of the changes for the project at large, helping future contributors along the way.*


If you have a very short message, you can record that with the -m flag and the message in quotes:

Example:
````bash
$ git commit -m "Updated Readme.md"
[main (root-commit) e024518] Updated Readme.md
1 file changed, 1 insertion(+)...
````

###### At this point, you can use the git push command to push the changes to the current branch of your forked repository:
Example:
````bash
$ git push --set-upstream origin new-branch
````   

### 5. Update Local Repository

*While working on a project alongside other contributors, it is important for you to keep your local repository up-to-date with the project as you don’t want to make a pull request for code that will cause conflicts. To keep your local copy of the codebase updated, you’ll need to sync changes.*

We’ll first go over configuring a remote for the fork, then syncing the fork.

### 6. Configure a Remote for the Fork

Next up, you’ll have to specify a new remote upstream repository for us to sync with the fork. This will be the original repository that you forked from. you’ll have to do this with the git remote add command.

````bash
git remote add upstream https://github.com/your-username/Team-9.git
````

In this example, `upstream` is the short name we have supplied for the remote repository since in terms of Git, “upstream” refers to the repository that you cloned from. If you want to add a remote pointer to the repository of a collaborator, you may want to provide that collaborator’s username or a shortened nickname for the short name.

### 7. Sync the Fork

Once you have configured a remote that references the upstream and original repository on GitHub, you are ready to sync your fork of the repository to keep it up-to-date.
To sync your fork, from the directory of your local repository in a terminal window, you’ll have to use the `git fetch` command to fetch the branches along with their respective commits from the upstream repository. Since you used the short name “upstream” to refer to the upstream repository, you’ll have to pass that to the command:

````bash
git fetch upstream
````

Switch to the local main branch of our repository:

````bash
git checkout main
Switched to branch 'main'
````

Now merge any changes that were made in the original repository’s main branch, that you will access through your local upstream/main branch, with your local main branch:

````bash
git merge upstream/main
````

### 8. Create Pull Request

At this point, you are ready to make a pull request to the original repository.

Navigate to your forked repository, and press the “New pull request” button on the left-hand side of your repository page.
![Create a new pull request](https://camo.githubusercontent.com/d5e050413f7273d4fe87ab6d855e810c8002eec2ad2d5e7fd7d4d30c18318412/68747470733a2f2f68656c702e6769746875622e636f6d2f6173736574732f696d616765732f68656c702f70756c6c5f72657175657374732f63686f6f73652d626173652d616e642d636f6d706172652d6272616e636865732e706e67)

## 🎉 Hurray! 🎉 
#### You just got closer to completing your Hacktoberfest challenge.