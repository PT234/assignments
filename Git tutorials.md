TUTORIAL ON GIT

Git  is a version control system for tracking changes in computer files and coordinating work on those files among multiple people. 
It is primarily used for source code management in software development,[8] but it can be used to keep track of changes in any set of files.
As a distributed revision control system it is aimed at speed,[9] data integrity,[10] and support for distributed, non-linear workflows

To use Git you will have to setup a repository. You can take an existing directory to make a Git repository, or create an empty directory
To make your current directory a Git repository we simply run init.
git init
Adding New Files
So we have a repository, but nothing in it. You can add files with the add command.
git add filename
To add everything in your directory try git add ..
Committing a Version
Now that we've added these files, we want them to actually be stored in the Git repository. We do this by committing them to the repository.
 
git commit -m "Adding files"


If you leave off the -m you will be put into an editor to write the message yourself.
Clone
git clone is a Git command line utility which is used to target an existing repository and create a clone, or copy of the target repository.
git clone ssh://john@example.com/path/to/my-project.git
cd my-project
# Start working on the project
The first command initializes a new Git repository in the my-project folder on your local machine and populates it with the contents of the central repository. Then, you can cd into the project and start editing 
files, committing snapshots, and interacting with other repositories. Also note that the .gitextension is omitted from the cloned repository. This reflects the non-bare status of the local copy.
Pull
The git pull command fetches changes from a remote repository to a local repository. It merges upstream changes in your local repository, which is a common task in Git based collaborations.
But first, you need to set your central repository as origin using the command:
git pull origin <branch-name>
Push
 
This command transfers commits from your local repository to your remote repository. It is the opposite of pull operation.

git push <remote> 

Fetch
$ git fetch origin


git fetch really only downloads new data from a remote repository - but it doesn't integrate any of this new data into your working files. Fetch is great for getting a fresh view on all the things that happened in a remote repository.


