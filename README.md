# git-quick-review
This is a quick guide of how to use git GIT , remember the most used commands start from how to connect to github, initialise the local repository, create new branches, switch between branches, and at the end cleanup brenshs.


	
This is a quick guide of how to use git GIT , remember the most used commands start from how to connect to github, initialise the local repository, create new branches, switch between branches, and at the end cleanup brenshs.

	1) Create a repositoy on github  git-quick-review
	When i create a new repository, the main branch created is called main
	2) sudo useradd gitlocaluser
	3) ssh-keygen  (on the current user from the local)
	4) cat .ssh/id_rsa.pub 
	5) Add key on github https://github.com/settings/keys
	6) mkdir gittest && cd gittest
	7) git init 
	8) git remote add origin git@github.com:omarhd66/git-quick-review
	9) git remote -v
	origin  git@github.com:omarhd66/git-quick-review (fetch)
	origin  git@github.com:omarhd66/git-quick-review (push)
	11) git fetch --all
	12) git branch -a
	* master
	  remotes/origin/main
	13) git branch -m main
	14) git branch -a
	* main
	  remotes/origin/main
	15) git pull origin main
		From github.com:omarhd66/git-quick-review
		 * branch            main       -> FETCH_HEAD
	11) ls -l
	README.md 
	12) git push origin main
	Everything up-to-date
	13) git branch -a
	* main
	  remotes/origin/main
	14) echo testo > testfile1
	15) git config user.email "git@quick-review.git"
	16) git config user.name "umer "
	17) git add .
	18) git status
	19) git commit -m "test commit 1"
	20) git push origin main
		
	


NEW BRANCH testbranch 
	1) git checkout -b testbadbranch 
		Switched to a new branch 'testbadbranch'

	2) git branch -a
		  main
		* testbadbranch
		  testbrach2
		remotes/origin/main
	3) git push origin testbadbranch 
	Total 0 (delta 0), reused 0 (delta 0), pack-reused 0
	4) git branch -a
	  main
	* testbadbranch
	  remotes/origin/main
	  remotes/origin/testbadbranch
	
	5) echo testo > testbadfile1
	 ls
	 README.md   testbadfile1   testfile1  
	6) git add .
	7) git status
	8) it commit -m "commit 1 testbadfile on testbadbranch branch"
	9) git push origin testbadbranch 

	


SWITCH BETWEEN BRANCHS
	1) git switch main
	ls
	README.md   testfile1 

	2) git switch testbadbranch 
	ls
	 README.md   testbadfile1   testfile1  

	3) git pull  origin testbadbranch
	From github.com:omarhd66/git-quick-review
	 * branch            testbadbranch -> FETCH_HEAD
	Already up to date.


CLEAN UP BRANCHS
Remove local branch:
git branch -a
	  main
	* testbadbranch
	  testbrach2
	  testbranch
	  remotes/origin/main
	  remotes/origin/testbadbranch
	  remotes/origin/testbrach2
	  remotes/origin/testbranch
git branch --delete testbrach2 
	Deleted branch testbrach2 (was 03c5bf7)
git branch --delete testbranch 
	Deleted branch testbranch (was e8649ab).
git branch -a
	  main
	* testbadbranch
	  remotes/origin/main
	  remotes/origin/testbadbranch
	  remotes/origin/testbrach2
	  remotes/origin/testbranch

Remove remote origin:
git push origin --delete testbranch
	To github.com:omarhd66/vprofile-projects-umer
	 - [deleted]         testbranch
git push origin --delete testbrach2
	To github.com:omarhd66/vprofile-projects-umer
	 - [deleted]         testbrach2

git branch -a
	  main
	* testbadbranch
	  remotes/origin/main
	  remotes/origin/testbadbranch

![image](https://user-images.githubusercontent.com/30199904/230269664-e083b353-2673-45f2-9a14-6d46d88e9822.png)
