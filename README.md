# Introduction to Git and GitHub

## Table of Content

1. [Setting Up a New Git Repository](https://your-link-here.com)
2. [Setting Up a New GitHub Repository](https://your-link-here.com)
3. [Git/ GitHub WorkFlow](https://your-link-here.com)
   
   -  [*Microsoft Visual Studio Code*](#microsoft-visual-studio-code)
   -  [*Useful Git Commands*](#useful-git-commands)
   -  [*Markdown Cheat Sheet*](#markdown-cheat-sheet)
     
   
#### Setting Up a New Git Repository

1. **Navigate to Your Project Directory**  
   - Windows: Open CMD and run the command `cd <directory>`. Alternatively, open a command prompt in the project folder.
   - Mac/Linux: Open Terminal and use the command `cd <directory>`.

2. **Initialize a New Git Repository**  
   Run the command `git init`. The command initializes a new Git repository in your current directory.

3. **Stage a `README.md` File**  
   Add the file to the staging area by running the command:
   ```bash
   git add README.md
   ```

4. **Commit Changes**  
   Run the command:
   ```bash
   git commit -m "Your commit message here"
   ```
   Replace "Your commit message here" with a description.

5. **Check Repository Status**  
   Check the status of your repository with:
   ```bash
   git status
   ```
   You should see `README.md` listed as modified or a new file.

6. **Stage All Changes**  
   Run:
   ```bash
   git add -A
   ```
   Alternatively, run `git status` again to see the changes. If `README.md` is untouched, you should see the output:
   ```
   On branch master
   Changes to be committed:
   (use "git restore --staged <file>..." to unstage)
           modified:   README.md
   ```

   #### Create a New Repository on GitHub**  
   Go to [GitHub](https://github.com) and create a new empty repository. Do not initialize it with a README.md, .gitignore, or license. Copy the repository URL.

1. Back in your terminal, add the remote repository URL using the command:
   ```bash
   git remote add origin <URL>
   ```
   Replace `<URL>` with the copied repository URL.

2. **Rename Your Branch**  
   Run:
   ```bash
   git branch -M main
   git push -u origin main
   ```

3. **Create** a `.gitignore` file and include necessary files and folders to be ignored by git. Alternatively, you can use a template from [GitHub's gitignore repository](https://github.com/github/gitignore) or generate one [at Toptal's gitignore generator](https://www.toptal.com/developers/gitignore).


4. **Commit** `.gitignore` 
   Stage and commit the `.gitignore` file using:
   ```bash
   git add .gitignore
   git commit -m "Added .gitignore file"
   git push --all
   ```
5. **Merge branches.**
   ```bash
   git checkout target-branch
   git merge source-branch
   git add .
   git commit -m "merged old branch with new"
   git push origin target-branch
   ```
. **When making changes to files...**
   ```bash
   git status
   git add <file>
   git commit -m "describe changes made"
   git push
   ```
<br>

 #### Optional: Delete the merged branch<br>

 If you don’t need the feature branch anymore

- Delete locally:
  
   ```git branch -d feature-login```

- Delete on GitHub:

   ```git push origin --delete feature-login```


## Various Git & GitHub Workflow

   * ##### Microsoft Visual Studio Code

      If you are using Visual Studio Code it can provide with some useful extensions for Git.
      <br>
      - [GitLens](https://marketplace.visualstudio.com/items?itemName=eamodio.gitlens): This extension helps with git commands and visualizations. It lets you see changes, commits, branches, and more directly in the editor.
      - [Git Graph](https://marketplace.visualstudio.com/items?itemName=mhutchie.git-graph): This extension provides a visual representation of your Git repository, allowing you to easily view branches, commits, and merges.
      - [Git Stash](https://marketplace.visualstudio.com/items?itemName=arturock.gitstash): This extension allows you to easily manage your Git stashes directly from Visual Studio Code.
      - [GitHub Copilot](https://marketplace.visualstudio.com/items?itemName=GitHub.copilot): This extension provides AI-powered code suggestions and autocompletions, which can help speed up coding and improve productivity.
      - [Markdown Preview Enhanced](https://marketplace.visualstudio.com/items?itemName=shd101wyy.markdown-preview-enhanced): This extension provides enhanced markdown preview capabilities, including support for diagrams, math, and more.
   <br>
   
   * ##### Markdown Cheat Sheet
      [Markdown Cheat Sheet](https://markdowncheatsheet.com/reference) Provides a comprehensive in-depth guide to markdown syntax, including extended features like tables, footnotes, and task lists.
   <br>
   
   * ##### Useful Git Commands
      The [Terminal Commands](./Terminal_Commands.md) file provides a couple of useful git commands for various tasks.

<br>---
  
#### Setting a New GitHub Repository

1. Navigate to [GitHub.com](https://your-link-here.com) <br>

2. Enter a Repository Name <br>

3. Description (optional) <br>

4. Click on `<Create Repository>`
   
   
#### Git/ Git WorkFlow

1. **Back to the Terminal**<br>
To connect your Local Repo to your Remote Repo with this command: <br>

```git remote add origin <URL>```

Replace the &lt;URL&gt; with the copied URL from GitHub. <br>

This wiil synch your Local Repo with your Remote Repo.

2. **Adding Udates to the Repos**<br>

- **Add changes to the Staging Area:** <br>
This command add push your changes to the staging area in your local repo.

  ```git add .```
  
- **Commiting Changes to the Local Repo:**

  ```git commit -m "add commit message" .```

- **To Check Repo Status:**

  ```git status```

- **To Check List of Commits:**

  ```git log```

- **Commiting Changes to the Remote Repo:**

  ```git branch -M main```

  ```git push -u origin main```

  
#### Cloning a Remonte Repository

1. Open the project in your remote repository

2. Click on the &lt;CODE&gt; the green button on your right conner of the page

3. Copy the &lt;URL&gt; 

4. Back &lt;Terminal&gt;, open the directory where you want the project to be saved &lt;cd directory name&gt;

5. Use the command &lt;git clone&gt; then paste the &lt;URL&gt; and &lt;Enter&gt;

The Repository is now saved in the Project Directory.


#### Create a .gitignore File

1. Create a .gitignore file inside your repository.
2. Open with Note Pad and add all the files you want to ignore
3. Use these command to stage and push the file:

  
  ```git add.ignore```
  
  ```git commit -m "commit message"```
  
  ```git push```


#### Branching 

1. Open the repo you want to create a branch

2. Click on &lt;main&gt; on the top-left  side of the page

3. Enter a branch name to create a branch


#### Merging

1. **Check out to the Branch you want to Merge int**:

   ```git checkout main```
   
3. **Update your Branch**:
   Pull the latest changes from GitHub so your branch is up to date:**

   ```git pull origin main```

5. **Merge the other branch into your current branch**

    ```git merge feature-login```

6. **Push the merged branch to GitHub**:

After merging locally, send the changes to GitHub

 ```git push origin main```

 #### Optional: Delete the merged branch<br>

- Delete locally:
  
   ```git branch -d feature-login```

- Delete on GitHub:

   ```git push origin --delete feature-login```

#### Collaborating with Pull Requests

1. Navigate the agithub repo using owners &lt;URL&gt;

2. On the Top Right hand Conner, click on &lt;Fork&gt;

3. Then below the page on the Right Conner, click on &lt;Create fork&gt;
   The Repo is forked to your github. Below &lt;Code&gt;, your will see &lt;sync fork&gt;

5. Make some changes and commit

6. Go to the forked repo and clkick on &lt;Pull requests&gt; at the top

7. Click on &lt;New pull request&gt;

8. Add your comments and then click on &lt;Comment&gt;

9. Otherwise if you want to close the pull request click on &lt;Close with comment&gt;

#### Revert and Reset

1. In Git, you can use two main tools to &lt;undo&gt; or &lt;back&gt;in your repository history:

Suppose you made a commit but want to undo it — without deleting history

- First, see your commit history:
  
   ```git log --oneline```

- Choose the commit you want to undo (e.g., a1b2c3d)

   ```git revert a1b2c3d```

This creates a new commit that undoes everything done in that commit.

Git might open your text editor to confirm the message — just save and close

Push the change:

 ```git push origin main```

Your repo now includes a new commit that reverses the unwanted change — without rewriting history.

   
&nbsp;

