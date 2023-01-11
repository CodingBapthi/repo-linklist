# Repo Linklist

This repository organizes a collection of git repositories as submodules, providing a convenient way to access them all without the need of forking them and consolidating them in a single place.

## Add a new repository as a submodule

1. Use the following command to add the repository as a submodule:
   git submodule add repourl name
   
2. Give the submodule a descriptive name that corresponds to the repository being added

3. Commit the changes by running the command:
   git commit -m 'Added name as a submodule'
   
4. Push the changes to the remote repository by running the command:
   git push

## Remove a submodule

1. Remove the submodule from the `.gitmodules` file. This file is located in the root of your repository and contains the configuration for all of the submodules. Open the file and remove the section that corresponds to the submodule you want to remove.

2. Remove the submodule's files from the repository. These will be located in a directory with the same name as the submodule in the root of your repository. You can use the command `git rm -r --cached path/to/submodule` to remove the files.

3. Commit the changes. Use the command `git commit -m "Removed submodule name"`

4. Delete the submodule's remote branch. `git push origin --delete branch_name` or `git push --delete origin branch_name` 

5. Finally delete the submodule folder from local repository
   `rm -rf path/to/submodule`