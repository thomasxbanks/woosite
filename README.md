# Nyamawoo's Site

## Sprint Zero - Setting up your environment.

1. Download a text editor (Atom, VSCode, Sublime Text). I recommend Atom because I'm most comfortable with it but the choice is yours. They all have pros and cons.
1. Download GitHub desktop. This will give you bash commands in windows - bash is used on linux (Apache) servers so is good to learn.
1. Download GitKraken. This is optional but can be useful for visual git learning and dealing with complicated merges.
1. Customise text editor (Pick a theme you are comfortable looking at for a long time. Colours indicate different functions of lines of code - called syntax highlighting. This will give you an idea of any mismatches or errors. My sync settings for Atom in gist)
1. Open GitBash and navigate to where you want to keep your projects. Use the bash commands: `cd` and `ls` to find your way around. __Pro Tip:__ `ls -asl` __lists things in a much better way than just__ `ls`
1. When you're in the right place, `mkdir woosite && cd $_` (create directory and change to it - $_ is last used variable)
1. `git clone http://github.com/thomasxbanks/express-boilerplate.git .` (the full stop indicates "this folder" which will stop a folder called "express-boilerplate being created inside woosite. You can also use it for general bash commands such as `ls .` to list everything in the current folder. Explain the benefits of using a boilerplate/seed.
1. Create a new repo in GitHub (http://github.com/nyamawoo).
1. `git remote set-url origin https://github.com/nyamawoo/woosite.git` to change remote from my repo to yours).
1. `npm i` (shorthand for install). Explain Node Package Manager.
1. Edit the `package.json` and explain JavaScript Object Notation and dependencies.
1. Update the `README.md` to reflect the new app. Otherwise (as happens to me __every time__!) your shiny app will have a boilerplate `README` and you'll look like a knob.
1. Explain Gulp and taskrunners. Go through the gulpfile and explain what each function does.
1. `npm start` - a catch-all function (defined in package.json) that will build a distribution folder, boot up the server, and start watching for changes in the code.
1. Now the `dist` folder has been created, go through the folder structure to explain where everything lives. Explain separation of concerns, templating, css architecture and naming conventions (ITCSS, Atomic, BEM, etc)
1. http://localhost:1337 (view the site locally)
1. If everything is up and running and looking good, we need to commit our changes to the new repo.
1. Open GitKraken and navigate to the repo folder.
1. You can see all the amends made to the repo since it was created. It's not very impressive yet (a single branch with a few commits) but it's going to get exciting
1. On the right, there are the files that have changed - called __Unstaged Files__. You can select them, add a commit message, and then click the big green button but... we're going to use bash to do it instead.
1. Switch back to GitBash, make sure you are in the same folder as your `.git` folder - This should be the root folder, in this case `woosite`.
1. `git stash` will put your changes in a sort of "holding area" to prevent merging issues.
1. `git pull` to get any changes made to the repo since you cloned/pulled it.
1. If none of the new files are files you have changed locally, `git stash apply` - Apply your changes from the holding area to the updated files.
1. `git add .` - Git will only `add` changed files so doing this in the root is a nice quick way of staging everything in one go.
1. `git commit -m "Updated the credentials"` - This is where you justify the reason for putting these files into the repo. In an ideal world, the message should be no longer than a tweet and contain your ticket number. In the real world, _"changes"_ or _"amends"_ are frequently used.
1. `git push origin master` - Because we haven't made any breaking changes to the codebase (this is basically your initial commit), we can use this command. This will put your changed files into the remote repo on the master branch.


## Sprint 1 - Your first change
1. Switch back to your text editor
1. Edit the _brand color_ in the css
1. Compile the changes (this should be done automatically if you are `watch`ing)
1. Refresh the browser and behold the changes!
1. Put your changes into the repo. You should know how to do this now.


## Sprint 2 - Your next change
1. Switch back to your text editor
1. Make some changes
1. Put the changes into the repo
1. Repeat for each change until you feel comfortable doing it


## Sprint 3 - Advanced Gittery
1. `git checkout -b hotfix`
1. Edit the _background color_
1. Check the changes are reflected in browser
1. `git diff` to see your changes to make sure nothing untoward has happened.
1. `git stash && git pull`
1. No changes? `git stash apply`
1. `git add .` to stage your changes
1. `git commit -m "Changed the background color"`
1. `git checkout master` - very important!
1. `git merge hotfix`
1. Add your merge message to explain why you need to merge the two branches. Welcome to the wonderful world of __Vi__!
1. `git push origin master` to send the new stuff up to the repo


## Sprint _n_ - Deploying to a server
1. Server
1. DNS, CNAME, A Records
