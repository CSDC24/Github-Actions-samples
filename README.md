# Github Actions samples

## What are Github Actions?

To summarize, Github Actions allow you to run certain **actions** like automatically running Unit/Integration tests, deploying software to servers, building software for distribution and more as a reaction to **Github** events like PR merges or pushes. That's where the name comes from.

**Note for private Repositories**:
Github offers [2.000 free build minutes](https://docs.github.com/en/billing/managing-billing-for-github-actions/about-billing-for-github-actions#included-storage-and-minutes) (usage multiplied by up to 10 depending on the action OS used) per month for free *per user account*. 
Github Actions have unlimited build minutes for public repositories. 
This should be enough for a few private repositories with a few actions (I have never run out of build minutes so far), but keep this limit in mind, especially if the Actions should suddenly stop working.

## How to use Github Actions

This repository contains some plug-and-play Github Actions that may be useful for your project. Feel free to open a Pull Request to add your own. 

To use a Github Action, simply place the configuration file in the ```.github/workflows``` subdirectory **of your repository root**. 
The Action will be executed the next time it is triggered. You can review the results of the action in the "Actions" tab on https://github.com.
Badges will also be added to commits in the commit history and Pull Requests if they triggered one or more actions.
For more information on how to write your own Actions, I recommend [you get started here](https://docs.github.com/en/actions/quickstart).
