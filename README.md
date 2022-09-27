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

Git Some Other Commands
-----------------------
               - git pull 
                           - git pull on the other hand does that AND brings (copy) those changes from the remote repository.
	       
	       
	      - git fetch
	              - git fetch is the command that tells your local git to retrieve the latest meta-data info from the original
		         (yet doesn’t do any file transferring. It’s more like just checking to see if there are any changes available).
	      - git merge






Git Remote Commands
----------------------
List the all remote branch 

		            - git remote -v  
		            - git branch -r
		            - git fetch origin 
			   
                               This fetches all the remote branches from the repository.
			       origin is the remote name you're targetting. So if you had an upstream remote name, you can call
				    
		           - git fetch upstream
		          
			   - git fetch --all
			   
Change the Branch  		

						  - git checkout -f origin/development



Reset The Git     
 
                                                  - sudo git reset --hard origin/development
						  - git rebase development
						  - git stash
						  - 
						  

Some Development Git Fix
========================
            1- When  Trying to checkout for one branch to another branch some error will be there 
		              |
			      |--------- git checkout file (all the file that modified on current branch)
			      |--------- rm -rf file (if that file is not required for current branch)
			      
            2- When some code not require on a branch and need to delete from branch(also code which present in branch and that branch already merged)
	                      |
			      |
			      |-----rm -rf folder(code/file)
			      |-----git add folder(code/file)(delete file ) 
			      |-----git comiit -m "file delete"
	     

						  

Git Error and Quick Fix  Commands
---------------------------------               
Error: Your local changes to the following files would be overwritten by checkout:
         
	 - git checkout -f development(You Branch Name)
	 - 

Support for password authentication was removed on August 13, 2021. Please use a personal access token instead.
----------------------------------------------------------------------------------------------------------------
                           
		
		   Create Personal Access Token on GitHub
		   Link -  https://stackoverflow.com/questions/68775869/support-for-password-authentication-was-removed-please-use-a-personal-access-to
		   
                    From your GitHub account, go to Settings => 
		                      Developer Settings => 
				            Personal Access Token => 
					    Generate New Token (Give your password) =>
					    Fillup the form => 
					    click Generate token => 
					    Copy the generated Token, it will be something like ghp_sFhFsSHhTzMDreGRLjmks4Tzuzgthdvfsrta






Common Flow
===========

                  First taking the git Clone
                       - git clone git@git.corp.adobe.com:acs-gdc-adobe-commerce-services/lgkorea-google-tag.git GoogleTag
		  
		  Going to that directory
                       - cd GoogleTag
		       - ls (code which is coming from master branch)
		       
		  Creating new Branch 
		       - git checkout -b GoogleTag           - here i am creating new branch bcz i need to put my code 
		       
		  
		  After checkout also i will get this master branch file inside my Custom branch
		       - sudo rm -rf Block/ etc/ registration.php  Setup/ view/                  -- so i am deleting from my custom created branch
		       
		  
		  After Delete Check the Files
		     
		       - git status                 --- deleted file details we will get here
		  
		  Adding this deleted details file
		   
		       -  git add .
		       
		  After adding the deleted file details Commiting the files
		  
		       - git commit -m "old deleted files "
		       
		  Pushing the Deleted Codes 
		  
		      - git push origin GoogleTag
		      
		 
		 -------------------Now Go to the Git Repo and Check the Details and Changes-----------------------------
		 
		 
		 This is the File Which i need to Keep to Our New Custom Branch Location
		 
		       - sudo cp -r /home/codilar/Documents/Adobe/GoogleTag
		       
		 Go to That File Location where we need paste 
		 
		      - sudo cp -r /home/codilar/Documents/Adobe/GoogleTag/*  ./
		      
		 
		 ------------------------------Now check the files - for all the changs files -----------------------------------
		 
		 
		      - git status
		      
		      - git add .
		      
		      - git commit -m "module refactoring"
		      
		      
		      - git push origin GoogleTag 

		    
		      

                 
      
		       
		       
When we are using Hyper-V On Windows -10
------------------------------------------

     - At the time of Connect to Putty 
                                     |---when we took the pull from git and when we try to get this remote file into local 
				                                    |
								    |---At that time we will get the some modified code error
								                      |
										    (Root User or Local User) -- So we get everytime modified file error
										    
You should be able to change the permissions (by terminal on the machine or over SSH) by running this so that users other than root can access it:
--------------------------------------------------------------------------------------------------------------------------------------------------
               - sudo chmod -R 757 /var/www
   (or)
           this so that it is owned by your user (which should be defined by $USER):
	   
                     - sudo chown -R $USER:$USER /var/www
		  
		    - sudo git config core.fileMode false
		     
You need to do this as only the owner+group can read, write and execute in /var/www, but other users can only read and execute - including the user you are using to try and the folders.

For more info, look at man chmod and man chown	

-----------------------------------------------------------------------------
		       
		     

			   
How To Resolve Git Conflicts & Why Git Conflicts Occurs
=======================================================
			
			
Issue - 1
----------
ssh: Could not resolve hostname github.com: Temporary failure in name resolution
fatal: Could not read from remote repository.

 Resolve -  Restart the Ssh
         -  Dis-connect the VPN Connection and Re-Connect with the WinSCP -->(Basically need to Disconnect the VPN and Give Permission (chmod -R 777 /var/www/html/)
		

Way to Solve
------------
          -> If Getting Conflict on branch 
	            |
		    |-> take the pull from that conflict branch and remove the conflict code


Issue -2
--------
           --> sudo git config --global --add safe.directory '*'
           --> sudo git config core.fileMode false

Issue -3
--------
          - ssh -T GITHUB-User_Name(Sanjay-cod34082)@github.com                ---> Check the git connection is success or not through ssh
	  - ssh-keygen -t rsa -b 4096 -C "cod34082@adobe.com"       ---> If ssh key is not generated use this to generated pub and private key
	
Issue -4
--------
         - If Accidentaly we did git  checkout  
	                      |-----------------for vs code do -- ctrl+Z to back the changes 
	                      |-----------------for vs code -  check on local history 
			      

	  
