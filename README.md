# GitHub Tutorial

_by Mohammad-Nadeem_

---
## Git vs. GitHub
**Git** is used by many people around the world. Git is used to monitor the changes that have been made to files. Git is a coding language that you can use to modify files. **Github** is a cloud based site were you can store all your files. You can aslo see the commits and changes you have made to your files. You can also collaborate with other people on the same files. You can also merge the changes your teamates have made.


---
## Initial Setup        
1. Open up Google Chrome by clicking the icon.
2. Go to [Github](https://github.com)
3. Sign up for a **Github** account 
4. Go to [Cloud9](https://c9.io)
5. Sign up for **C9**
6. Create a new workspace
7. Check your email you used for the sign ups and confirm your accounts if they are needed.
8. Go back to **Github**, log in if you haven't. Click on your profile icon on the top right corner. Click on settings, on the left you should see SSH and GPG keys. Once there click on "New SSH key" and title it cloud9.
9. Switch over to c9.io log in if you haven't. On the top right you should see a gear icon click it. Go to SSH key tab and copy the private SSH key given to your account. Copy the SSH key and go back to Github, paste the key in the key box and click add SSH key.
10. Go back to c9.io open up the workspace you have created and type this command "ssh -T git@github.com". If you have succesfully done this you should get a message "Hi (your username)! You've successfully authenticated, but GitHub does not provide shell access".

---
## Repository Setup
Making your first repo can be pretty exciting. After a couple of times creating repos you get used to it.
1. Open up c9.io and go to your workspace.
2. To create your first repo you should be under workspace. Make sure where you are about to type, towards the left it says (yourusername):~/workspace. Go ahead and type mkdir (your first repos name). Mkdir stands for make a directory which creates a folder so you can create files in that folder
3. After that go into the folder by typing **cd** (your first repos name). The meaning of cd is change directory and it changes your directory. You use cd to navigate around the folders your have created.
4. When you cd to your folder the first thing you should do is **git init**. This command initializes git inside the folder so you can start coding.
5. We can get started by creating your first file, type **touch** (filename). The touch command creates a new file under the folder you are in. Open up the file and type anything you want
6. After you have modified your file type **git add** (filename). Git add gets the file for a commit so you can finalize the changes. Afer this type **git commit** -m 'Any message you want but make it meaningful'. Git commit -m '' finalizes the changes you have made to the file. 
7. Before you can push you have to create a repo on github.com. Go to github.com and on the top right you should see a + icon click on it and click new repository. The name should be the same as the repo you created in c9.io. So if you named your repo first-repo on c9 it should also be first-repo on github. After naming the repo click create repo.
8. After you have done that you should see a screen that says quick setup. Make sure you have SSH click on the top of this page. Copy one of the two commands on the bottom of the page they look similar to this "git remote add origin git@github.com:username/reponame.git" and "git push -u origin master".   
9. Copy the commands one at a time. Copy the first command "git remote add origin git@github.com:username/reponame.git" and paste it in your repo that you have created. This command creates a bridge between your c9.io repo and remote repo on github.com. Then copy and paste the second command "git push -u origin master". This command makes it that if you do git push it will be pushed to the remote repo on github. 
10. Now just type **git push** to push the changes you have made to your remote repo you just created.




---
## Workflow & Commands
Using basic workflow commands are necessary for using git. The basic command are git status, add , commit, push
* git status checks the status of the files in the repo if they have been added or not. 
* git add, adds the files to the staging area and makes them ready for commit
* git commit -m '' commits the changs you have made and finalizes the changes you have made it.
* git push pushes the changes you have made to your remote repo.

 

---
## Rolling Back Changes
* To undo git add use git reset.
* To erase a commit entirely and go back to the pervious commit use 'git reset -- hard HEAD ~1'. To not get rid of your files and index use "git reset -- soft HEAD~1" You can also use 'git revert' to go back to a pervious commit
* To undo a commit use 'git reset -- hard HEAD ~1' which goes back to the pervious commit and then force push by using 'git push -f'.