# git
Git Tutorials 

git remote add {custom name} [path of the repo]

git fetch {custom name}

git pull {custom name} [branch name 'sandbox']

git push origin [fork branch name]

create a pull request.

# terminal password change 
git config credential.helper cache


# Reset to a previous commit 

 git log
 
 git reset --hard <log name> // looks like "da6595a5f0b4bb62c27db74b7a0716bfc1698ca5"
 
 git push -f origin <branch name>
 
 git pull <remote -alzheimer-> <branch name -sandbox-lazy->
 
 
 #Saving Changes with Git Stash
 
 "git stash --help"
 
 check if we have any existing stashes.  
 
 "git stash list"
 
The list option shows all of the existing stashes, if there are any. If you do have some they’ll be listed like this:
stash@{0}: .....
stash@{1}: .....
stash@{2}: .....
Each stash is listed in a separate line, starting with the stash name that consists of the word “stash” and an index (starting with zero) in curly braces. The latest stash is the one at the top, with the index of zero (confusing, right?).

Let’s add a stash. To do that we use the stash savecommand.

'stash save "updated the offline file"'

To apply a stash to the working directory, we have a couple of options. The first is:

"git stash pop"

which will remove the most recent stash from the list and apply it to the current working directory. It’s just reversing what you did when saving the stash (but keeping any subsequent repository changes intact).

You can also be specific and pop any stash in the list:
"git stash pop stash@{1}"

The other option when applying a stash is to use:
"git stash apply"
Just like with pop, we can choose to not specify a stash and it will use the latest. Or, we can specify one, like this:

"git stash apply stash@{1}"
With apply, we’ll get similar output when applying the stash, but without the message that the stash was dropped. Why? Because git stash apply applies the stash we specified but it doesn’t drop it from the list of stashes.

 
 
