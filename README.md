# git-intro: A brief introduction to Git

Git is a nice way to store and track changes for source code.  You
have come across this repo/file, and you need to use Git... what do
you need to know to get started?

## Getting Git

To get started, you need the program, Git. On GNU/Linux, the program
is either already installed (try typing `git --version` in the
Terminal), or just a call of your package manager away, with (Assuming
Debian based distros, others, you know enough to figure this out
already.)

```
sudo apt-get install git
```

Once you have the program, you are ready on the local side.

## Get Remote

One of the benefits of Git is distributed development, so to leverage
that, you need a central repository to store the code. One such place
is [Github](https://github.com). Others exist, and you could even make
your own, but we'll ignore the other options for now.

Set up an account on GitHub. I believe in you. Choose a user name that
is sane, and you wouldn't mind putting on a business card. For
example, my GitHub handle is [@jnclark](https://github.com/jnclark).

## Create a repo

With your newly minted GitHub account, log in and you'll be greeted by
your dashboard (or whatever they call the main page now.)

1. Find the **New** button on the page.

2. Click it. You'll be greeted by **Create a new repository**.

3. Fill in the required fields.

  - Pick a descriptive name, that is not too long.
  - Also pick Public or Private access.
  - Additionally, initialize the repo with a README. This will help in a second.

4. **Create Repository**

## Getting to work

To begin work, you need to *clone* your newly created repo.

1. Open the terminal emulator of your choice.

2. Navigate to the folder you wish to clone your repo into (your
cloned repo will make its own folder with your repo name as its name)

  - Use `ls` to view the folders where you currently are located,
  - Use `cd Folder` to enter a folder you like, or
  - Use `mkdir UniqueFolder` to make a new folder for yourself.

3. Once you are situated, type out
`git clone https://github.com/yourusername/reponame.git`
and press enter. You may need to authenticate with your password,
depending on your repo and github settings.

> You can make this more convenient with **SSH** keys, which requires
a slightly different URL. If you are interested, give it the ol'
internet search.

4. In your terminal, `cd reponame` You are now in a local copy of your
remote repo.  Alternatively, you can also just navigate into the
folder using your file manager.

## Get Git to work

0. To begin, `git pull` to get your repo up to datte, compared to the
remote repo.

Make a file for your project. Edit the README to contain the general
structure of your project. Once you have made some edits, and saved
your local changes, you will need to send your changes to the remote
repo. To do so,

1. You need to add any new files that you have not yet started
tracking, and make any changes you have made to extant files. Luckily,
this uses the same command. `git add file.txt` You can check the
status of your changes with `git status`

2. Commit (to) your changes Make the Git repo add the changes to its
version history `git commit` This will open an editor for you to
document the changes.

> Even if only doing this for yourself, it is a good idea to keep a
good record of the changes, so if you need to go back for whatever
reason, you can have a general idea of where to look based on the
commit messages. When working in teams, there is even more use for
these commit messages.

3. Push it to remote All you need here is to `git push` and all your
committed local changes are reflected in your remote repo.

## Rinse and repeat

Don't forget to `pull` (before working), `add`, `commit`(after making
your changes) and `push` (when you are done).

# Where from here?

This is just about the minimum you need to start using Git. There are
many extremely useful features that are available.

1. Explore comparing commits on the web and locally.

2. Look into **SSH** for authentication.

3. Try setting a .gitignore to ignore (in `git status`) the
automatically generated files (such as PDFs) or other files you wish
to ignore in your project. An example .gitignore is available in this
repo. (Locally, files prefixed with a . are hidden.)

4. Merging and other collaborative features such as forking, et cetera.

5. And much much more.