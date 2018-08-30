# teamstory
A collaborative story written by our class.

# Instructions for Team Story on Github
Team Story is a GitHub repository that you can use as a starting point for practicing using Git and GitHub. 
The repository has a basic story in it. We need everyone to help complete the story by adding parts to it.
Follow the instructions to perform various tasks, such as forking, cloning, and updating a repository.

This exercise is inspired by http://opensourcerer.diy.org/ which contains step-by-step DIY guides teaching beginners how to do various tasks in Git and GitHub.


### Fork
First we create a **remote** copy (that means it's stored on Github.com) of a project on our account that stays linked to the original (because we want our changes to affect this original). This is called a **fork**

1. Log into GitHub and go to [https://github.com/ivonetafe/teamstory](https://github.com/ivonetafe/teamstory).
2. Near the top right, click `Fork`. This means we're creating a copy of the code onto our account that will be linked to the original on ivonetafe's account. 


### Clone 
Now that we've forked the files to our Github account, we need to **clone** (aka copy) them so that we have a local version of the files on our computer (this means we can work on them while offline). Our clone will be linked to our fork which is linked to the original.


## Open Bash
1. Open a new command line window in git bash.

2. Let's create a folder that will hold all of our code files. Bash is starting us at the root of our computer, but let's move into our Documents folder.

To navigate to another folder, we need to *change directories* or **cd**. Here are the Mac and Windows commands:

    cd Documents
    
or

    cd My\ Documents/
    

Then create a new folder with **mkdir** - *make directory*. Type:

    mkdir teamstory
    
Great! But we're still inside of the Documents folder, so let's go into teamstory:

    cd teamstory
    

### Clone the Repo
3. Tell Git to go to Github repository on the internet where we are storing our forked files and clone them to where we are right now inside of the teamstory folder. Each repo on github has an address for its location. You'll see it following the HTTP and SSH buttons near the top middle of the page. Click on HTTP, this is the address you'll use. 

**Tip** the http address will look like this: https://github.com/YOURUSERNAME/teamstory.git 
By default our fork's name is *origin* and it is on the *master branch*. 

Type:

    git clone https://github.com/YOURUSERNAME/teamstory.git

Watch as it copies the files! It will also create a folder for you with the name of the repo. When it's done cloning, move into the repo's folder:

    cd teamstory

Now we're inside our very own copy of the files. Let's use **ls** to *list* the contents of this folder to see what we've got!

    ls

You should see a set of filenames that look exactly like the files you see on the website for both ivonetafe and your account page.

### Connect to Original
4. We have one last thing to do. Because this is an open project, we can expect that may others will be doing the same as us: forking and cloning and making changes to the files. We want to make sure we're always working with the most up to date files. To ensure this, we'll connect our local copy to the ivonetafe original so that we can **pull** in the most recent changes before we work on ours. If you go back to the ivonetafe page for teamstory, you'll see the HTTP address in the near the top middle: https://github.com/ivonetafe/teamstory. We're going to name this connection *upstream*.

Type

    git remote add upstream https://github.com/ivonetafe/teamstory
    
### Pull Changes
5. Before we make any additions, we want to make sure we have the latest files by pulling in any changes from the *master* branch *upstream*.

Type

    git pull upstream master

If it says 'Already up to date' then no changes have been made since you started setting up! If there were changes, it updated your files. In both cases, your files will match the files on the original owner's Github.

### Edit the File
Now let's add our part to the story! We can also open up a file from Bash.

Type

    open collaborative-story.txt
    
It should open up the file in your computer's text editor. Add your own portion of the story after the last sentence.

When you're done, save the file. Make sure you keep it saved as a .txt file. 

### Push Changes
Now let's add our changes to our forked copy and then submit them to be added to the owner's original file. 

Return to Bash and let's check what changes we've made. Type

    git status
 
This shows you what files you've made changes to - it should say `collaborative-story.txt`. Let's see the *difference* before and after our changes with **diff**. 

    git diff
    
You'll see a plus and minus sign showing the before and after.

Add Changes
Tell Git what file you want to add.

    git add collaborative-story
    
**Pro tip** if you have multiple files and want to add them all, you'll type `git add .` The period means *all*.

### Commit Changes
Now we'll add a *message* describing our changes and attach that to our push.

    git commit -m "your description of changes"
    
### Push Changes to our Fork
Now, finally, we'll actually push our file and message to our fork on Github. Remember our fork's name is origin (it's our *original* file) and the branch is *master*.

    git push origin master
    
### Pull Request
Now our local (computer) version and our fork on Github match. Let's submit our changes to ivonetafe to be added to the original. We're **requesting** they **pull** our changes into their files.

You do this part online. If you go to your forked version on Github's website, you'll see a button near the top right `Pull Request`, click this.

You'll be taken to a page that shows ivonetafe's original on the left and your fork on the right. Fill out the form to describe to ivonetafe what it is you're suggesting they add and then click `Send pull request`.

Now ivonetafe staff will get an alert of your request, be able to see your changes and merge them into the original. Now when the next user forks or pulls and update of this repo, they'll get your updates too!

WOW! You've just forked, pulled, pushed and pull requested like an open source programming pro!

This walk through was long, but we did a lot of setting up. Now, if you wake up one day with some story inspiration, all you need to do is use Bash to navigate back to your folder and pull any updates that have been made since you last checked the files:

    git pull upstream master

Then open up the text file and make changes. Save your changes and then:

    git push origin master
    
Next, go to your Github page for the repo and select Pull Request. You've done it again!


