# HomeWork-Lesson2
Clone remote repository
![clone_repo](images/1.png)

Create and checkout to my-updates branch
![checkout_my-updates](images/2.png)

Create file survey.html
![create_file](images/3.png)

Add the file in the working directory to the staging area and capture a snapshot of the project's currently staged changes

![add_commit](images/4.png)

Add more commits to my-updates history
![more_commits](images/5.png)

Viewing an old revision
**git checkout**
Make working directory match the exact state of the previous commit 98e21ad
![checkout](images/6.png)

As a result, commit history looks like:
![commit_history](images/7.png)

To get back to the “current” state of our project:
![current_state](images/8.png)

Push changes to remote repository
![push_origin](images/9.png)

**git clean**
Create some files and directories to track and untrack
![clean_command](images/10.png)

Perform a “dry run” of git clean to show which files are going to be removed without actually removing them

![clean_dry_run](images/11.png)

This commands shows untracked directories too
![git_status](images/12.png)

Perform git clean with options to remove files and directories separately
![clean_f_df](images/13.png)

**git clean -di**
Create some files and directories to untrack again and see git status
![git_status](images/14.png)

Interactive mode or git clean interactive
![clean_interactive](images/15.png)

**git revert**
![revert](images/16.png)

Revert latest commit and as a result “prepend line content” line was removed from file

![revert_head](images/17.png)

Output git status
![git_log](images/18.png)

**git reset**
Create reset_lifecycle_file, add the file to the staging area and make a commit
![touch_add_commit](images/19.png)

*The working directory*
![status](images/20.png)

*Staging index*
The git ls-files command is essentially a debug utility for inspecting the state of the Staging Index tree

![ls-files-s](images/21.png)

The object SHA for reset_lifecycle_file has been updated from e69de29bb2d1d6434b8b29ae775ad8c2e48c5391 to d7d77c1b04b5edd5acfc85de0b592449e5303770

![git_add_status](images/22.png)

*Commit history*
![git_commit_am](images/23.png)

**git reset --hard**
Create a new file named new_file and add it to the repo. And modify the content of reset_lifecycle_file:

![create_new_file](images/24.png)

Examine the state of the Staging Index
![status](images/25.png)

After git reset –hard command we can see that state of Index Stage has been reset to a point before new_file was added. Modifications to reset_lifecycle_file and the addition of new_file have been destroyed.

![reset_hard](images/26.png)

**git reset --mixed**
Again, add a new_file and modify the contents of reset_lifecycle_file. These changes are then applied to the Staging Index with git add

![git_add_status_ls-files](images/27.png)

Execute the reset –mixed
![reset_mixed](images/28.png)

The Staging Index has been reset to a state where reset_lifecycle_file is the only file in the index. The object SHA for reset_lifecycle_file has been reset to the previous version. The Staging Index has been reset and the pending changes have been moved into the Working Directory.

**git reset --soft**
Add reset_lifecycle_file and commit 
![add_commit_reset_file](images/29.png)

View commit history before git reset --soft
![commit_history](images/30.png)

git reset –-soft d253b13
![reset_soft](images/31.png)

Commit Tree was moved back by one commit
![reset_soft_status](images/32.png)

**git commit –-amend**
View git status
![status_before_commit_amend](images/33.png)

Use git commit –amend to add new_file to commit
![status_before_commit_amend](images/34.png)

**git rebase**
Create and swith to the new branch featureB from main 
![status_before_commit_amend](images/35.png)

Make several commits at featureB branch
![navbar_commits](images/36.png)

Push changes to the remote repository
![git_push_origin_featureB](images/37.png)

Checkout to main and update it
![git_checkout_main](images/38.png)

Checkout to my-updates branch and make changes to it
![git_checkout_my-updates](images/39.png)

Create two commits
![nano_new_file](images/40.png)

Current commit history at my-updates branch 
![commit_history](images/41.png)

Make git rebase from main to get missing commits
![git_rebase](images/42.png)

After rebase command changes from featureB branch appear at my-updates branch right beneath two new commits made before this command 

![git_log](images/43.png)

Besided previous commits SHA changed from
![git_log_before](images/44.png)
to
![git_log_after](images/45.png)
**rebase -i**
Add 5 files to repo and commit changes. As a result we have 5 commits
![git_commit_log](images/46.png)

Some of them are in wrong order and have typo that can be corrected with rebase -i
![git_log](images/47.png)

Make git rebasase -i 767a66d command with commit hash just right before problem occurred and next window is open

![git_rebase_window](images/48.png)

Then use command pick to change the order of commits and reword to edit commit message

![git_pick_reword](images/49.png)

Then commit message can be changed in the opened window
![git_edit](images/50.png)

Finally here is such commit history
![git_log](images/51.png)

Then squash all five commits into one with squash command
![git_squash](images/52.png)

Squash four commits at the top one
![git_squash_command](images/53.png)

As a result here is one commit instead of five
![git_squash_command](images/54.png)

