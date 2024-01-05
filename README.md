# Git and Github Codes
How to push Existing Code to a new Github repository

Example Empty Repo
1. Run **"git init"** in the terminal. *(This will initialize the folder/repository that you have on your local computer system.)*
2. Run **git add .** in the terminal. *(This will track any changes made to the folder on your system, since the last commit. As this is the first time you are committing the contents of the folder, it will add everything.*
3. For the first time, configure user email
    - **git config user.email "Email used in Github"**
    - **git config user.name "Username used in Github"**
4. Run **git commit -m"insert Message here"**. *This will prepare the added/tracked changes to the folder on your system for pushing to Github. Here, insert Message here can be replaced with any relevant commit message of your choice.*
5. Create a new repo in Github and copy the repo link of HTTPS or SSH
6. Run **git remote add origin https://github.com/username/example.git or git@github.com:username/example.git** in the terminal. *Here, username and example will be replaced by the values provided in the copied link. This will push the existing folder on you local computer system, to the newly created Github repository.*
Here the 'origin' can be either HTTPS or SSH
7. Run **ssh-keygen -t rsa -b 4096 -C "email_ID_of_GITHUB"** and "**save in default location**". Default location:
   - In windows "C:\Users\PC-Name\.ssh". *It is done for the first time to configure SSH connection*
   - In Ubuntu "
9. If you performed **step7**, then copy the Public Key saved in **.\\.ssh\\*.pub** file and save it in your **SSH and GPG key** section of Github account.
10. Run **git remote -v**. *This does some git pull and git push magic, to ensure that the contents of your new Github repository, and the folder on you local system are the same.*
11. Run **git push origin master**. *Note that the last word in the command master, is not a fixed entry when running git push. It can be replaced with any relevant “branch_name”.*
---------------------------------------------------
### Useful codes
- create a .gitignore file to exclude files
--------------------------
