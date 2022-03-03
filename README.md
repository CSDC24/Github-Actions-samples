# Github Actions samples

Credits: Stefan Schindler

## What are Github Actions?

To summarize, Github Actions allow you to run certain **actions** like automatically running Unit/Integration tests, deploying software to servers, building software for distribution and more as a reaction to **Github** events like PR merges or pushes of commits. That's where the name comes from.

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

## Customize the sample Actions

Each Action consists out of different parts, but the most important ones are described below:

- ```name```: defines the name that will be shown on Github
- ```on```: defines the [events](https://docs.github.com/en/actions/using-workflows/events-that-trigger-workflows) that trigger the Action.
The following provide a good starting place for deployments and test execution:
    - ```pull_request```: runs every time a Pull request is created or updated.
    Useful for automatically running tests during the PR review process.
    - ```push```: runs every time commits are pushed to Github.
- ```jobs```: defines the Actions to be executed.
  ```runs_on``` defines what OS to use (keep this in mind as non-linux OSs consume more build minutes).
  For more information on how to write your own Workflow, see [Getting Started with Github Actions](https://docs.github.com/en/actions/quickstart).

# Feedback & Questions

I hope that these samples will help you improve and automate your workflows and, in the end, write better, cleaner code faster.
I'd be happy to hear your feedback and help you with questions.
Contact me via the CSDC Discord!
