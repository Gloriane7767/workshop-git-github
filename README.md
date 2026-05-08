# Introduction to Git and GitHub

## Table of Content

1. [Setting Up a New Git Repository](#setting-up-a-new-git-repository)
2. [Setting Up a New GitHub Repository](https://your-link-here.com)
3. [Git/ GitHub WorkFlow](https://your-link-here.com)
   
   -  [*Microsoft Visual Studio Code*](#microsoft-visual-studio-code)
   -  [*Useful Git Commands*](#useful-git-commands)
   -  [*Markdown Cheat Sheet*](#markdown-cheat-sheet)
     
   
## Setting Up a New Git Repository

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


## Create a New Repository on GitHub**  
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


 ## Optional: Delete the merged branch<br>

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
   
   
   * ## Markdown Cheat Sheet
      [Markdown Cheat Sheet](https://markdowncheatsheet.com/reference) Provides a comprehensive in-depth guide to markdown syntax, including extended features like tables, footnotes, and task lists.
   <br>

   
   * ## Useful Git Commands
      The [Terminal Commands](./Terminal_Commands.md) file provides a couple of useful git commands for various tasks.

---
  
