# Git-Standards
Things that I've picked up from git over the years.

  
## Branching

  
### Preface:

  
Going through the a few git repos, I’ve noticed that a lot of teams aren't using issues or pull requests. I’ve grown accustomed to a way of creating branches based on what issues are open, naming them accordingly, and then submitting a pull request to be peer reviewed, make suggested changes, then let the reviewer merge the code in.

  
### Practice:

  
When I was getting started with proper git etiquette, I used [git flow](https://www.atlassian.com/git/tutorials/comparing-workflows/feature-branch-workflow). This works well for some teams, but I’ve developed a style of branching that keeps things clean, up to date, and very easy to follow.

  
1. Anything you want to add to the repo, you add as an issue. Here’s an example of a repo I’m working on: 
![Screen Shot 2015-05-12 at 11.25.40 PM.png](https://lh3.googleusercontent.com/CTQrWspKBfxFnFs1YkXP1GWMv2J3sLtdyD-h8afHCKWpgJB08-RoSscrJ8E2p5KUTEvU_Iye8KcT6tQZkukf1jU1nCuH0Gk9N1W1fRaNTkuN38yP2zqL44dApfbfT38hDv0sg2A)

2. When creating an issue, it’s imperative to add tags like “bug”, “enhancement”, “feature”, “needs qa”, and any steps you may have in your development process to differentiate issues and segment them. Not doing this defeats the purpose of opening issues as they are all uniform otherwise. You should also assign issues to team members with milestones so that each person knows exactly what they’re working on and when it should be completed by. 
![Screen Shot 2015-05-12 at 11.28.03 PM.png](https://lh5.googleusercontent.com/zeqpVxn3nhxEbvMhjZMa_144FzxFBKig4iZw6FzXYw4pMlAIEu9mK6CBGroXvvQ6JjDwuJgmJMotWSh8Uu1hLhBwnUuLzwTmaj3jjPzT82Qosu1NIGmtKqJ7cWo18vurtTygsRE)


3. Then, when you want to work on something: choose an issue, make a branch beginning with either bugs/, enhancements/, or features/. Then append the issue number, and a description of the issue. Examples include:



  1. bugs/87-archives-crash-app


  2. bugs/92-font-size-update-not-immediate


  3. enhancements/56-add-date-search


  4. enhancements/63-show-number-tweets-in-search-results



4. Once you’ve written the code AND TESTED YOUR FEATURE THOROUGHLY, submit a pull request against whatever branch you were based off of (likely development or staging). It is the job of one of your peers to go through your code and review it, make suggestions, and allow you to update your code. NO REVIEWER SHOULD EVER MODIFY THE CODE IN THE PULL REQUEST, THE ONE WHO SUBMITTED THE PULL REQUEST SHOULD BE 100% RESPONSIBLE FOR THEIR FEATURE. Pull requests can look like this: 
![Screen Shot 2015-05-12 at 11.35.50 PM.png](https://lh4.googleusercontent.com/J5mAk0jKUtobNaArALuJ1nVy8MtPPShCUGMq6hc_ZWEM_zHelJaQ-5db33n7c2DRCdS5hE745n-QiHVLgaoCNE5TZLOrLpc_fMP43nq17AqoCAqE8svRSGhFk6ka04BI7R_k_tU)


5. When the reviewer is satisfied with the code, they can then merge it into whatever it’s based off of. This keeps everyone in the loop with what code is being written where.



  
  
##Cleaning your branches

  
###Preface:

  
I noticed that a lot of repos have dozens of unused or stale branches

  
###Practice:

  
A lot of these branches have random names that nobody can identify with. For instance, 

what is "suresh_test", that branch isn't helpful to anyone and should be a local branch. Getting rid of all this unused code will help people keep better track of what has been merged in and what is a work in progress. There’s a branch in here that’s over 4,000 commits behind master, I’d recommend deleting similar branches.

  
  
##Committing

  
###Preface:

  
There’s a standard for commit messages I’ve adopted from colleagues and friends. There does not seem to be any uniformity between all the commit messages I see in this repo.

  
###Practice:

  
Commit messages should always begin with a [present tense verb](http://stackoverflow.com/questions/3580013/should-i-use-past-or-present-tense-in-git-commit-messages) and be spell checked, this prevents people from rushing commits and giving you messages like this: "remvoed linkedin gemspc from bunlder"

  
The reason for it being in present tense is that when you look back on the commit or cherrypick it, you know that when you remove this commit or revert to it that it will "Remove LinkedIn GemSpec from the bundler."
