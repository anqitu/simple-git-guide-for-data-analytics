## A Simple Git Guide for Data Analytics

### 1. Code Branching Practices
- **Main branch**: For our repositories, the main branch is named **develop**. When we make code changes, we eventually want them to be merged to this main branch. However, since this branch is important, only the moderators can merge to this branch directly.
- **Feature branch**: To keep your code changes separate and safe from the main branch, you should always create a `feature` branch and add your code changes there. The `feature` branch should always have a prefix of `feature/` (i.e., feature and slash character). Give a meaningful name to your feature branch. For example: `feature/recognize_face`.
- **Merge to main branch**: After you have finished implementing your feature or fixed your bug in your feature branch, give a pull request on Github. Request the moderators of the repository to review your code and merge it to the main branch.

### 2. Standard Pull Request Workflow
> All the steps below can be done with a git client (eg. [GitKraken](https://www.gitkraken.com/)) or via [command line](https://gist.github.com/Chaser324/ce0505fbed06b947d962#file-github-forking-md)
#### 2.1 Clone a Repository
Head over to the GitHub page of project repository and clone the repository to your local machine.

Step 0: Create a repo on github
- **Skip** if there is already a repo on github (as for Pandas' case here)
- **Recommend** separate words by '-' instead of space
![step_1_0_create_a_repo](/screenshots/step_1_0_create_a_repo.png)

Step 1: Copy web URL from Github repository page
![step_1_1_copy_web_URL](/screenshots/step_1_1_copy_web_URL.png)

Step 2: Select 'Clone Repo' in GitKraken
![step_1_2_clone_repo](/screenshots/step_1_2_clone_repo.png)

Step 3: Paste web URL and configure project path (highly recommend you to to have a folder dedicated to put all your coding projects)
![step_1_3_configure_path](/screenshots/step_1_3_configure_path.png)

Step 4: Finish cloning the repo to your local memory
![step_1_4_finish_clone](/screenshots/step_1_4_finish_clone.png)

Step 5: Make sure you switch to the develop branch instead of the master branch ()
![step_1_5_switch_to_develop_branch](/screenshots/step_1_5_switch_to_develop_branch.png)

#### 2.2 Creating a Branch
Whenever you begin work on a new feature or bug fix, it's important that you create a new `feature` branch. Not only is it proper git workflow, but it also keeps your changes organised and separated from the `develop` branch so that you can easily submit and manage multiple pull requests for every task you complete.

Step 1: Click on **Branch**
![step_2_1_click_branch](/screenshots/step_2_1_click_branch.png)

Step 2: Enter a meaningful branch name which is always in the format of ```feature/xxxxx```.
![step_2_2_branch_name](/screenshots/step_2_2_branch_name.png)

Step 3: Press ```Enter``` and there are several changes here.
- There exists a branch in your local memory
- You have been switched to the ```explore_data``` branch
- There are some files appeared in the **Unstaged Files** section, together with a notification - 'a file change in working directory - View change'
![step_2_3_local_branch](/screenshots/step_2_3_local_branch.png)

Step 4: Click on the **View change**, you will see the files that has been changed (Usually it is the **code** you have added or modified in any scripts, but the change here is the **new branch** you have created). Click on **Stage all changes**.
![step_2_4_branch_change](/screenshots/step_2_4_branch_change.png)

Step 5: The changed file will move to the **Staged Files** section. Write some meaning description of this commit in the **Commit Message** section. Then click on **Commit changes**.
![step_2_5_commit_message](/screenshots/step_2_5_commit_message.png)

Step 6: The local repo has the new branch already, but the remote Github repo still has not been updated with the new changes and does not have the new branch. So click on **Push**  to push changes to remote Github repo..
![step_2_6_commit_local](/screenshots/step_2_6_commit_local.png)


Step 7: Click on **Submit**
![step_2_7_push](/screenshots/step_2_7_push.png)

Step 8: Push the changes successfully. Now the change is in both local and remote. Local and remote repo are also synchronized now.
![step_2_8_push_successfully](/screenshots/step_2_8_push_successfully.png)

Then, here you go. You can start working on writing codes for this branch, but always remember to push your codes to this branch. **Make sure your GitKraken is always on this branch. Do not push to other branches.**
![step_2_9_make_sure_branch](/screenshots/step_2_9_make_sure_branch.png)


#### 2.3 Cleaning Up Your Work
After completing the codes for this feature you are working on, you would want to merge it with the upstream ```develop``` branch. Prior to submitting your pull request, you might want to do a few things to clean up your branch and make it as simple as possible for the moderators to test, accept, and merge your work.

Thus, If any commits have been made to the upstream `develop` branch, you should **rebase** your `feature` branch or merge the upstream 'develop' branch into your own so that merging it will be a simple fast-forward that won't require any conflict resolution work.

To do so, click on **Fetch**, then resolve any possible conflicts appeared, commit and push all changes to this ```feature/xxxx``` on Github.
![step_3_fetch](/screenshots/step_3_fetch.png)

#### 2.4 Submitting a Pull Request
Once you've committed and pushed all of your changes to this ```feature/xxxx``` on Github, make a **Pull Request** to merge your brach into the upstream `develop` branch.

Step 1: Click on **PULL REQUEST+**
![step_4_1](/screenshots/step_4_1.png)

Step 2: Configure the request setting - from the ```feature/xxxx``` branch to the ```develop``` branch. Click on **Create Pull Request**.
![step_4_2](/screenshots/step_4_2.png)

If you need to make any adjustments to your pull request, just push the updates to GitHub. Your pull request will automatically track the changes on your `feature` branch and update.


### 5. Download Data
Step 1: Download data from Kaggle and put into your repo folder.
![step_5_1_download_data](/screenshots/step_5_1_download_data.png)

Step 2: Go to GitKraken. As you have added data to the working directory, you will see the **View changes** reminder.
![step_5_2_view_changes_for_data](/screenshots/step_5_2_view_changes_for_data.png)

Step 3: Right click on one of the file, select 'Ignore', then 'All files in 'data/'.
![step_5_3_ignore_data](/screenshots/step_5_3_ignore_data.png)

Step 4: Select **Ignore and Stop Tracking**. As such, all future files in the 'data' folder will be ignored by GitKraken and would not appear in the **Unstaged Files** section.
![step_5_4_conform_ignore_and_stop_tracking](/screenshots/step_5_4_conform_ignore_and_stop_tracking.png)
