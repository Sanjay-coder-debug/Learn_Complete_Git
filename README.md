# Learn_Complete_Git
All Git Command and use 


---------------------------------

# Git-Command
all git command


## Git Commands
1. **git init**: for linking your folder with an empty repository.

	    git init
2. **git clone**: for using the exiting repository and working on it.

	    syntax: git clone <repo-name> <directory>
	    Example: git clone https://github.com/sanjay-codez/Git-Command.git app 
3. **git config**: for configuring the git info such as user name , email and all.
		

	    Example:
	    git config –global user.name “sanjay-codez”
	    git config –global user.email “sanjay.d@gmail.com”
4. **git add**: for adding the files to git 

        syntax: git add <file>
        Example:
	    git add code/Codilar/Merchant
5. **git commit**: In Simple words git commit is like a storing of code in a separate space where all the things you commit are tracked.
		
		syntax: 
		       git commit -m "Message"
		       git commit --amend -m "Change the Message"
        Example:
	    git commit -m "[feature/merchant] Merchant Module Added"
6. **git branch**: This command lists all the local branches in the current repository.
		
		syntax: 
		       git branch #shows list of branch present
		       git branch -D <branch-name> #deletes the branch
7. **git checkout**: This command is to switch and create the branches
		       
       syntax: 
		       git checkout <branch-name> #switch to the existing branch
		       git checkout-b <new-branch-name> #switch to new branch by creating it.
		       git checkout <file-name> #removes the modified content or file.   
		       git checkout-b <new-branch-name> <reference-branch>
		       (Switch to a new branch by keeping the reference).
       Example: 
		       git checkout -b feature/merchant development
Note: 
**Why do we require branch model?**

		 

> Lets assume you are writing a code, for a feature called mobile login, initially the requirement would be for mobile login for all the country. you wrote code by considering all the country code, you may have finished 80% of work, later client says we are  just releasing this phase in India so lets finish it fast only do it for India. So you have to remove 40% code and make changes, tomorrow the client says they decided to release in all the country so they require the feature, so you would have to rework and build it.

> Instead of doing this if you create a new branch(feature/merchant-v1.0) from the feature/merchant, then tomorrow you can pull from the existing and continue the work.

**Branch Model**
		       
<img width="818" alt="git1" src="https://user-images.githubusercontent.com/78407424/134554267-a0822d15-b73b-48df-a2af-bcd57df37ee4.png">

<img width="818" alt="git2" src="https://user-images.githubusercontent.com/78407424/134554581-6e76718a-fe94-4eb4-bc65-63ce91521356.png">


8. **git diff**: This command is to check the difference between the current code and previous commit.
		       
       syntax: 
		       git diff  #when you want to check diff across all the files. 
		       git diff <file-name> #when you want to check difference in a specific file
       Example: 
		       git diff
		       git diff code/Codilar/merchant/etc/frontend/di.xml
		       
9. **git push**: This command is to push the commit to your respective branch
		       
       syntax: 
		       git push origin <branch-name> #when you have to push the origin repository
		       git push <remote-name> <new-branch-name> #when you to push to a remote repository.).
       Example: 
		       git push origin feature/merchant

Note: Some other important commands such as git reset, git stash, git rebase are used when we add a file to git by mistake and we want to fix it or revert it.
1. [Rebase](https://git-scm.com/docs/git-rebase/en)
2. [Stash](https://git-scm.com/docs/git-stash) 
3. [Reset](https://git-scm.com/docs/git-reset)


# ==================================================

Git Remote Commands
----------------------
*List the all remote branch 
		                                - git remote -v  
		                                - git branch -r
		      
		           - git fetch origin 
			   
			            = This fetches all the remote branches from the repository. origin is the remote name you're targetting. So if you                                                    had an upstream remote name, you can call
				    
		           - git fetch upstream
		          
			   - git fetch --all
			   
*Change the Branch  				
						- git checkout -f origin/development






	  
