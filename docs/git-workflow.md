# Git Workflow Guide

## Introduction

This document outlines a formal Git workflow for efficient code management and collaboration. Follow these steps from the project's root directory in your terminal.

## 1. Checkout main branch
Execute the following command to switch to main branch if not already.

```
git checkout main
```

## 2. Obtain Latest Repo.

If you already have a local copy of the repository then synchronize with the latest changes using

``git pull``

**Note:** Always make sure you are using the latest copy of the repo before you start working on any kind of task because this will mitigate merge conflicts once you are ready to push your code to the repo.

## 3. Create a Feature Branch

To develop a new feature or address a specific task, create a dedicated branch to isolate changes. Choose a descriptive branch name that indicates the purpose of your work. Use the following command to create a new branch and switch to it:

``git checkout -b new_feature_branch``

## 4. Implement Changes

Once on the feature branch, implement the necessary code changes and modifications. Use Git commands to track the status of files:

``git status``

Verify that all changes appear correctly under the "Untracked files" section.

## 5. Stage Changes

Before committing your work, stage the specific files that you want to include in the commit. It is recommended to stage files selectively rather than adding all changes at once. Use the following command to stage files:

``git add <file_path>``

Alternatively, to stage all changes, use:

``git add .``

## 6. Commit Changes

After staging your changes, create a commit with a clear and descriptive message that explains the changes made. A well-crafted commit message enhances readability and facilitates future reference. Use the command:

``git commit -m "Commit Message"``

## 7. Push to Remote

**Note**:  If the branch named **new_feature_branch** already exists in the remote repository, ensure to fetch the latest changes before proceeding with further updates. You can achieve this by executing:

``git pull origin new_feature_branch``

Once the commit is ready, push the feature branch and its associated changes to the remote repository using:

``git push -u origin new_feature_branch``

This will create ```new_feature_branch``` in the repo. The -u flag adds it as a remote tracking branch after which you can do just ```git push``` to push changes from local ```new_feature_branch``` to remote ```new_feature_branch```.

## 8. Create a Pull Request

Pull requests let you tell others about changes you've pushed to a branch in a repository. Once a pull request is opened, you can discuss and review the potential changes with collaborators and add follow-up commits before your changes are merged into the **main** branch. Its advised **not** to merge your **new_feature_branch** directly into **main** or any other branch without undergoing this review process. Follow the following steps to Open a Pull request:

1. Open the Repository in Github.
2. On top you can find **Compare & pull request** button.
3. Fill all the details and click **Create pull request** to open a pull request.

## 9. Resolving Conflict in PR

Once the PR is created and shows some conflicts, simple follow the below steps to resolve the conflicts:

1. Open the Pull Request
2. Navigate to Conflicts tab
3. Make necessary changes
4. Click on Resolve and submit.

**Note:** Merge conflicts can be resolved using several different ways.

## 10. Clean-up

Its always a good practice to delete the **new_feature_branch** from the repository as well as locally after it is **successfully merged** with the **main** branch of the repository.

**Note:** Ensure you are in the main branch or any other branch that is not the **new_feature_branch**.

To delete the **new_feature_branch** from the repository execute the folllowing command:

``git push origin --delete new_feature_branch``

To delete the **new_feature_branch** locally execute the folllowing command:

``git branch -d new_feature_branch``
