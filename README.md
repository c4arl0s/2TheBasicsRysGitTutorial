# [go back to content](https://github.com/c4arl0s/RysGitTutorial#rys-git-tutorial) 

# [2. The Basics - Content](https://github.com/c4arl0s/2TheBasicsRysGitTutorial#go-back-to-content)
 * [Create the example Site](https://github.com/c4arl0s/2TheBasicsRysGitTutorial#-create-the-example-site)
 * [Initialize the Git Repository](https://github.com/c4arl0s/2TheBasicsRysGitTutorial#-initialize-the-git-repository)
 * [View the repository status](https://github.com/c4arl0s/2TheBasicsRysGitTutorial#-view-the-repository-status)
 * [Stage a snapshot](https://github.com/c4arl0s/2TheBasicsRysGitTutorial#-stage-a-snapshot)
 * [Commit the Snapshot](https://github.com/c4arl0s/2TheBasicsRysGitTutorial#-commit-the-snapshot)
 * [View the repository History](https://github.com/c4arl0s/2TheBasicsRysGitTutorial#-view-the-repository-history)
 * [Configure Git](https://github.com/c4arl0s/2TheBasicsRysGitTutorial#-configure-git)
 * [Create New HTML files](https://github.com/c4arl0s/2TheBasicsRysGitTutorial#-create-new-html-files)
 * [Stage the New Files](https://github.com/c4arl0s/2TheBasicsRysGitTutorial#-stage-the-new-files)
 * [Commit The new Files](https://github.com/c4arl0s/2TheBasicsRysGitTutorial#-commit-the-new-files)
 * [Modify the HTML Pages](https://github.com/c4arl0s/2TheBasicsRysGitTutorial#-modify-the-html-pages)
 * [Stage and Commit the Snapshot](https://github.com/c4arl0s/2TheBasicsRysGitTutorial#-stage-and-commit-the-snapshot)
 * [Explore the Repository](https://github.com/c4arl0s/2TheBasicsRysGitTutorial#-explore-the-repository)
 * [Conclusion](https://github.com/c4arl0s/2TheBasicsRysGitTutorial#-conclusion)
 * [Quick Reference](https://github.com/c4arl0s/2TheBasicsRysGitTutorial#-quick-reference)

# [2. The Basics](https://github.com/c4arl0s/2TheBasicsRysGitTutorial#2-the-basics---content)

- This module explores the fundamental Git workflow: creating a repository, staging and committing snapshots, configuring options, and viewing the state of a repository.

# 	* [Create the example Site](https://github.com/c4arl0s/2TheBasicsRysGitTutorial#2-the-basics---content)

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <title>A Colorful Website</title>
  <meta charset="utf-8" />
</head>
<body>
  <h1 style="color: #07F">A Colorful Website</h1>
  <p>This is a website about color!</p>    
  
  <h2 style="color: #C00">News</h2>
  <ul>
    <li>Nothing going on (yet)</li>
  </ul>
</body>
</html>
```

# 	* [Initialize the Git Repository](https://github.com/c4arl0s/2TheBasicsRysGitTutorial#2-the-basics---content)

```console
$ cd /Users/carlossantiagocruz/SWIFT-PROGRAMMING/RysGitTutorial
```

- then initialize

```console
$ git init
```

- output

```console
Initialized empty Git repository in /Users/carlossantiagocruz/Documents/SWIFT-PROGRAMMING/RysGitTutorialRepository/.git/
```

# 	* [View the repository status](https://github.com/c4arl0s/2TheBasicsRysGitTutorial#2-the-basics---content)

```console
$ git status
```

```console
On branch master

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
	index.html

nothing added to commit but untracked files present (use "git add" to track)
```

- Git does not automatically track files because there are often project files that we don't want to keep under revision control.

# 	* [Stage a snapshot](https://github.com/c4arl0s/2TheBasicsRysGitTutorial#2-the-basics---content)

- tell git to start tracking index.html

```console
$ git add index.html
```

```console
$ git status
```

- output

```console
On branch master

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
	new file:   index.html

```

- A snapshot represents the state of your project at a given point in time.
- Git's term for creating a snapshot is called staging
- Staging give us the opportunity to group related changes into distinct snapshots.

# 	* [Commit the Snapshot](https://github.com/c4arl0s/2TheBasicsRysGitTutorial#2-the-basics---content)

```console
$ git commit
```
![Screen Shot 2020-05-22 at 12 55 58](https://user-images.githubusercontent.com/24994818/82695901-9b39ba80-9c2b-11ea-9542-d3499c0dc735.png)

# 	* [View the repository History](https://github.com/c4arl0s/2TheBasicsRysGitTutorial#2-the-basics---content)

```console
$ git log
```

- output

```console
commit 6a442fcc4ab51362713f09ed5eadc7af767db833
Author: c4arl0s <c.santiago.cruz@gmail.com>
Date:   Fri May 22 12:54:21 2020 -0500

    Create index page for the message
```

# 	* [Configure Git](https://github.com/c4arl0s/2TheBasicsRysGitTutorial#2-the-basics---content)

```console
$ git config --global user.name "your name"
$ git config --global user.email your.email@example.com
```

[read book if you want more information]

# 	* [Create New HTML files](https://github.com/c4arl0s/2TheBasicsRysGitTutorial#2-the-basics---content)

- orange.html

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <title>The Orange Page</title>
  <meta charset="utf-8" />
</head>
<body>
  <h1 style="color: #F90">The Orange Page</h1>
  <p>Orange is so great it has a
  <span style="color: #F90">fruit</span> named after it.</p>
</body>
</html>

```

- blue.html

```console
<!DOCTYPE html>
<html lang="en">
<head>
  <title>The Blue Page</title>
  <meta charset="utf-8" />
</head>
<body>
  <h1 style="color: #00F">The Blue Page</h1>
  <p>Blue is the color of the sky.</p>
</body>
</html>
```

# 	* [Stage the New Files](https://github.com/c4arl0s/2TheBasicsRysGitTutorial#2-the-basics---content)

```console
$ git add orange.html blue.html
```

```console
$ git status
```

- output

```console
On branch master
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
	new file:   blue.html
	new file:   orange.html

```

![Screen Shot 2020-05-22 at 13 21 50](https://user-images.githubusercontent.com/24994818/82697808-3d0ed680-9c2f-11ea-9c17-f8f3009351dd.png)

# 	* [Commit The new Files](https://github.com/c4arl0s/2TheBasicsRysGitTutorial#2-the-basics---content)

```console
$ git commit -m "add blue and orangle html file"
```

![Screen Shot 2020-05-22 at 13 47 10](https://user-images.githubusercontent.com/24994818/82699708-c1af2400-9c32-11ea-800a-1b578fcbcac5.png)

# 	* [Modify the HTML Pages](https://github.com/c4arl0s/2TheBasicsRysGitTutorial#2-the-basics---content)

- add this at the end of index.html

```html
<h2>Navigation</h2>
<ul>
  <li style="color: #F90">
    <a href="orange.html">The Orange Page</a>
  </li>
  <li style="color: #00F">
```

- add this at the end of orange.html

```html
<p><a href="index.html">Return to home page</a></p>
```

# 	* [Stage and Commit the Snapshot](https://github.com/c4arl0s/2TheBasicsRysGitTutorial#2-the-basics---content)

```console
$ git status
```

- output

```
On branch master
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
	modified:   index.html
	modified:   orange.html

no changes added to commit (use "git add" and/or "git commit -a")
```

-

```console
$ git add index.html orange.html blue.html 
```

- status

```console
On branch master
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
	modified:   index.html
	modified:   orange.html

```

- commit 

```console
$ git commit -m "Add navigation links"
[master 453c8a4] Add navigation links
 2 files changed, 10 insertions(+), 1 deletion(-)
```

- Note that the red circle, which represent the current commit, automatically moves forward every time we commit a new snapshot.

![Screen Shot 2020-05-22 at 16 55 24](https://user-images.githubusercontent.com/24994818/82712156-0d6ec700-9c4d-11ea-8dd1-8f705f6996ae.png)

# 	* [Explore the Repository](https://github.com/c4arl0s/2TheBasicsRysGitTutorial#2-the-basics---content)

```console
$ git log --oneline
```

- output

```console
453c8a4 Add navigation links
1047951 t Add blue an orange html files
6a442fc Create index page for the message
```

- Condensing output to a single line is a great way to get a high-level overview of a repository
- Another useful configuration is to pass a filename to git log:

```console
1047951 t Add blue an orange html files
```

- This display only  the blue.html history.
- Notice that the initial Create index page commit is missing, since blue.html didn't exist in that snapshot.


# 	* [Conclusion](https://github.com/c4arl0s/2TheBasicsRysGitTutorial#2-the-basics---content)

![Screen Shot 2020-05-22 at 17 01 45](https://user-images.githubusercontent.com/24994818/82712586-f086c380-9c4d-11ea-9896-d302b0345e8a.png)

# 	* [Quick Reference](https://github.com/c4arl0s/2TheBasicsRysGitTutorial#2-the-basics---content)

```console
$ git init
```

Create a git repository in the current folder.

```console
$ git status
```

View the status of each file in a repository.

```console
$ git add fileName
```

Stage a file for the next commit.

```console
$ git commit
```

Commit the staged files with a descriptive message.

```console
$ git log
```

View a repository's commit history.

```console
$ git config --global user.name "<nameOfTheUser>"
```

Define the author name to be used in all repositories.

```console
$ git config --global user.email <email>
```

Define the author email to be used in all repositories.

