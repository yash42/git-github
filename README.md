# Git and Github Codes
How to push Existing Code to a new Github repository

Example Empty Repo
1. Run **"git init"** in the terminal. *(This will initialize the folder/repository that you have on your local computer system.)*
2. Run **git add -A** in the terminal. *(This will track any changes made to the folder on your system, since the last commit. As this is the first time you are committing the contents of the folder, it will add everything.*
3. For the first time, configure user email
    > **git config user.email "Email used in Github"** </br>
    > **git config user.name "Username used in Github"**
4. Run **git commit -m"insert Message here"**. *This will prepare the added/tracked changes to the folder on your system for pushing to Github. Here, insert Message here can be replaced with any relevant commit message of your choice.*
5. Create a new repo in Github and copy the repo link of HTTPS or SSH
6. Run **git remote add origin https://github.com/username/example.git or git@github.com:username/example.git** in the terminal. *Here, username and example will be replaced by the values provided in the copied link. This will push the existing folder on you local computer system, to the newly created Github repository.*
Here the 'origin' can be either HTTPS or SSH
7. Paste the text below, replacing the email used in the example with your GitHub email address.
   > **ssh-keygen -t ed25519 -C "your_email@example.com"** 
   - If you are using a legacy system that doesn't support the Ed25519 algorithm, use:
   >  **ssh-keygen -t rsa -b 4096 -C "email_ID_of_GITHUB"** </br>
    and "**save in default location**".
   - Default location:
    >   - In windows "C:\Users\userprofile\\.ssh\". *It is done for the first time to configure SSH connection* </br>
    >  - In Ubuntu ""
    -----------------
    **To connect multiple account with multiple ssh key** </br>
   - If you are using OpenSSH for Windows 10 with PowerShell, you can create the config file yourself by running the following command in PowerShell: </br>
   > ***Open powershell in default ssh location and type the code*** </br>
   > New-Item -Path $HOME\\.ssh\\config -ItemType File 
   - Open config file and write down the following code:
    > Host github.com </br>
    >> HostName github.com </br>
    >> User *githubaccount* </br>
    >> IdentityFile ~/.ssh/*custom_ssh_key* </br>
    and save it.
    ---------------------------
9. If you performed **step7**, then copy the Public Key saved in **.\\.ssh\\*.pub** file and save it in your **SSH and GPG key** section of Github account.
10. Run **git remote -v**. *This does some git pull and git push magic, to ensure that the contents of your new Github repository, and the folder on you local system are the same.*
11. Run **git push origin master**. *Note that the last word in the command master, is not a fixed entry when running git push. It can be replaced with any relevant “branch_name”.*
---------------------------------------------------
### Useful codes
- create a .gitignore file to exclude files
- Change default branch from <b>master</b> to <b>main</b>
    >> git config --system init.defaultbranch <i>main</i>
--------------------------
