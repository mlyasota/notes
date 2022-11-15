</br>

```
Title: GitHub Notes
```

</br>

<h1>Table of Contents</h1>

- [git-init-clone-config](#git-init-clone-config)
- [git-push-pull](#git-push-pull)
- [git-branches](#git-branches)
- [PULL Request through Command Line](#pull-request-through-command-line)
- [git-request-pull](#git-request-pull)
- [Other Links](#other-links)

<div style="page-break-after: always; break-after: page;"></div> 

</br>
<!-- # Making branch
    git switch -c task1 
    git branch -a
    git commit -m 'task 1 partially complete'
    git push --set-upstream origin task1 -->

# [git-init-clone-config](https://www.atlassian.com/git/tutorials/setting-up-a-repository)
-

</br>

# [git-push-pull](https://www.datacamp.com/tutorial/git-push-pull)
<h2> push </h2>


<h2> pull request </h2>

- The simple command to PULL from a branch is:
  ```
  git pull 'remote_name' 'branch_name'
  ```

</br>

# [git-branches](https://www.theserverside.com/blog/Coffee-Talk-Java-News-Stories-and-Opinions/git-push-new-branch-remote-github-gitlab-upstream-example)
1. Clone the remote Git repo locally
   ```
   git clone https://github.com/mlyasota/srt521-project-phase-1.git
   ```
2. Create a new branch with the branch, switch or checkout commands
   ```
   git switch -c new-branch-name
   ```
   - To verify what branch you are on, use:
     ```
     git branch -a
     ```
3. Perform a git push with the --set-upstream option to set the remote repo for the new branch
   ```
   git push --set-upstream origin new-branch-name
   ```
4. Continue to perform Git commits locally on the new branch


5. Simply use a git push origin command on subsequent pushes of the new branch to the remote repo

</br>

# [PULL Request through Command Line](https://www.datacamp.com/tutorial/git-push-pull)
<h2> 1. Fork the Repository</h2>

> This step needs to be completed on githubs website. There is __*NO*__ terminal command offered by 'git' to fork.

<h2> 2. Clone the forked repo </h2>

<h2> 3. Make a new branch </h2>

```
git checkout -b 'branch_name'
```

<h2> 4. Make your changes to the source files </h2>

<h2> 5. Add and Commit a file to the repository </h2>

- Add
  ```
  git add README.md
  ```
- Commit
  ```
  git commit -m 'Fixed typo in README'
  ```

<h2> 6. Push the repository to GitHub </h2>

```
git push origin 'branch_name'
```

</br>


# [git-request-pull](https://git-scm.com/docs/git-request-pull)

<h2> <b>NAME</b> </h2>

git-request-pull - Generates a summary of pending changes

<h2> <b>SYNOPSIS</b> </h2>

```
git request-pull [-p] <start> <URL> [<end>]
```

<h2> <b>DESCRIPTION</b> </h2>

Generate a request asking your upstream project to pull changes into their tree. The request, printed to the standard output, begins with the branch description, summarizes the changes and indicates from where they can be pulled. </br>
The upstream project is expected to have the commit named by ```<start>``` and the output asks it to integrate the changes you made since that commit, up to the commit named by ```<end>```, by visiting the repository named by ```<URL>```.

<h2> <b>OPTIONS</b> </h2>

```
-p
  Includes patch text in the output.
<start>
  Commit to start at. This names a commit that is already in the upstream history.
<URL>
  The repository URL to be pulled from.
<end>
  Commit to end at (defaults to HEAD). This names the commit at the tip of the history you are asking to be pulled.
```
When the repository named by ```<URL>``` has the commit at a tip of a ref that is different from the ref you have locally, you can use the ```<local>:<remote>``` syntax, to have its local name, a colon ```:```, and its remote name.

<h2> <b>EXAMPLES</b> </h2>

Imagine that you built your work on your ```master``` branch on top of the ```v1.0``` release, and want it to be integrated to the project. First you push that change to your public repository for others to see:
```
git push https://git.ko.xz/project master
```
Then, you run this command:
```
git request-pull v1.0 https://git.ko.xz/project master
```
which will produce a request to the upstream, summarizing the changes between the ```v1.0``` release and your ```master```, to pull it from your public repository. </br>
If you pushed your change to a branch whose name is different from the one you have locally, e.g.
```
git push https://git.ko.xz/project master:for-linus
```
then you can ask that to be pulled with
```
git request-pull v1.0 https://git.ko.xz/project master:for-linus
```





# Other Links


> [Create a Self-Hosted GitLab Server From Your Linux PC](https://betterprogramming.pub/create-a-self-hosted-gitlab-server-from-your-linux-pc-2738bc6538d2)

> [5 open source alternatives to GitHub](https://opensource.com/article/20/11/open-source-alternatives-github)
1. GitLab
2. Gitolite
3. Gitea and Gogs
4. Independent communities
5. [Git](https://github.com/git/git)

<!-- - Push a new Git branch to a remote repo
    > The steps to follow in order to push new Git branches to remote repos such as GitHub, GitLab or Bitbucket are as follows:
  1. Clone the remote Git repo locally
  2. Create a new branch with the branch, switch or checkout commands
  3. Perform a git push with the –set-upstream option to set the remote repo for the new branch
  4. Continue to perform Git commits locally on the new branch
  5. Simply use a git push origin command on subsequent pushes of the new branch to the remote repo
- New branch to remote Git repo commands
- New Git branches and upstream repos
- New Git branch pushed to GitHub
- Ongoing push and pull commands for GitHub -->

