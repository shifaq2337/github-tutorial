# GitHub Tutorial

##### _by Shifa Quddus_

---
## Git vs. GitHub
Git is the version control, git commands are used to take screenshots of code. This does not require GitHub and it runs in the command line.    
GitHub is used to store the screenshots from local repositories into the cloud. This requires Git.  
The difference between git and GitHub is that git is the version control and GitHub is the place where the commits made using git in a local repository is saved. 

---
## Initial Setup
1. Go to the [GitHub](https://github.com) website.
2. Click the sign up button.
3. Type a username and password you can remember.
4. Click the Free Account plan.
5. After you are done, check your email and verify with Github (by clicking on the link sent in the email).
6. Go to c9.io and sign in to cloud9 using your Github account.
7. After signing into cloud9, press the gear icon on the top-right, then press the Connected Service button. You will see Github listed, and right next to that you will see the green button Connect, press Connect (to connect GitHub and cloud9).  

SSH Key  
1. Go to GitHub, on the top-right click on the profile icon then settings.  
2. Next, on the left-sidebar click on SSH and GPG Keys. Then, click on New SSH key to make a new SSH key.   
3. Put cloud9 as the title. Then, go to cloud9, press the gear icon, press the SSH keys tab, copy(from cloud9) and paste the SSH key in GitHub and add the SSH key.

---
## Repository Setup
1. Create a folder or repository by using either the command line (`mkdir foldername`) or by clicking on the left-sidebar and then clicking New Folder. 
2. After creating the folder change from workspace to the new folder (`cd foldername` into the folder). 
3. Then, initialize git in the new repository by typing the command `git init foldername`. Go ahead and make a README file in the folder by typing the command `touch README.md`. 
4. Now, open the `README.md` file (by clicking on it or by typing `c9 README.md` in the command line), type something, and save the file. 
5. Then, type `git status` just to make sure git realizes that you made changes in a file. Type `git add README.md` to add the file to the stage and then type `git commit -m "message that tells you in present tense what changes you made"`.
6. Now, you have to set a remote repository on GitHub before pushing your commits to GitHub. Go to GitHub, on the top-right press the + button and press the New Repository button. Name the repository on GitHub the same name as the repository on cloud9 and create the repository. Make sure to click SSH, copy and paste into cloud9 the one that says `git remote add origin git@github.com : yourgithubusername/repo-name.git`. Then, copy and paste into cloud9 : `git push -u origin master`. 


---
## Workflow & Commands
* `git status` is used to see since the last commit made, which files have been edited (filenames that appear Red tells you that git detected that you edited a file and did not add the file to the stage to commit and the filename appears green if it was added to the stage). Correct syntax : `git status` 
* `git add` is used to add (edited or new) file(s) to the stage to be committed. Correct syntax : `git add filename`  
* `git commit -m "relevant/specific message"` is used to save a screenshot of the code that was modified in a file and added to the stage. A relevant and clear message is useful to know what changes you made, in case you want to refer back to the specific code later on (the message should be in present-tense). Correct syntax : `git commit -m "relevant/specific message"`    
* `git push` is used to upload commits made in the local repository to the remote repository. Correct syntax : After, doing `git push -u origin master` in one repository just typing in `git push` works in that repository.


