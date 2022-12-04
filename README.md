# Basic GitHub Instructions
We use GitHub to host our code with version control, continuous integration, and colloboration. 

[You'll need to install git on your development machine](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git)

Before you submit your code to a repository you will want to remove any passwords, tokens, client ids, or other credentials and private information from your code. This can be done with environment variables. [Click here to learn how to set up environment variables.](https://github.com/Website-Stuff/github-basics/blob/main/basic_environment_variables.md)

## Creating an Access Token

You’ll need an access token to push and pull code. Visit https://github.com/settings/tokens/new

Check “repo” and then generate token.

This token is your password for pulling and pushing code to repos.

You can also get there the long way:

- Click your profile picture in the top right corner of GitHub.com
- Settings
- Developer settings on the left side of the screen
- Personal access tokens
- Generate new token


## Creating a new Repository

Click “New Repository”

Provide a name for your repository

Add a .gitignore file for whatever language you’re programming in. Probaly Python

Click “Create Repository”

That’s it, You’ve created a new repository.




## Clone Repo to Server or Development Environment

Now that your GitHub repository is setup you’ll want to clone it on the machine you wish to run it on. 

Get the URL of our GitHub repository by clicking the “Code” button in the repository and copy the URL.

!['clone'](https://github.com/Website-Stuff/github-basics/blob/main/clone.png)

Start by cloning it on a development server or your local machine. In a terminal navigate to a folder where you want to store your files. 

Clone the repository with the following command in a terminal (change the url to the correct url for your repo):

```
$ git clone https://github.com/YOURACCOUNT/your_repo.git
```

If the repo is private you will have to enter your username and password.  Your password is the token you generated earlier.

That's it, you're done! You have copied the repo to your machine.

After cloning the repo you will see a new folder with the repo name and any files it contains within.


  
  
## Push Code to Repo:

Once you’ve made changes to the code on your development machine you should push the updates to the GitHub repo. 
 
This is a great way to back up your code in case of disaster. It also keeps track of changes over time and records contributions you make. Push often!
 
If you are developing on a server you should run the following commands before pushing. (Change the credentials to your own). If I don’t do this on my development machine the updates get credited to Ubuntu.
 
```
$ git config --global "user.name" "YOUR NAME"
$ git config --global user.email 12345667+YOURUSERNAME@users.noreply.github.com
```
 
From within the folder in a terminal add the files:
```
$ git add *
```

Then submit commits with a short message that describes the updates you’ve made
```
$ git commit -m "amazing new feature"
```

Then push the code to GitHub with the name of the branch. 
```
$ git push origin main
```

You will be prompted for your username and password. The password is your token, not your GitHub password.
 
That’s it, your code is now updated on GitHub.
 
 
## Push Code to New Branch:


Check out new branch
```
$ git checkout -b <branch>
```

Add files
```
$ git add *
```

Then submit commits with a short message that describes the updates you’ve made
```
$ git commit -m "amazing new feature"
```

Push to new branch
```
$ git push origin <branch>
```


## Pull Code from Repo:
 
If you want to update a machine running older code like a production server or other development server you can run the pull command. To do so you must open a terminal on the machine you want to pull the code to, navigate to folder with the existing code, and run:

```
$ git pull 
```

You will be prompted for your username and password. The password is your token, not your GitHub password.
 
That’s it, your code is now the newest code from GitHub.
