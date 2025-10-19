## Create a new branch 
![[Pasted image 20251019164106.png]]

## Make a small change and push the branch to Github
![[Pasted image 20251019164316.png]]

## Open a Pull Request on GitHub
![[Pasted image 20251019163953.png]]

## Review an existing PR
![[Pasted image 20251019164742.png]]
PR link: https://github.com/facebook/react/pull/34755

## Why are PRs important in a team workflow?
Pull requests add structure to the workflow followed in a team by enforcing a structure of adding changes to a repo where teammates have to 'request' for their changes to be merged with a branch and someone has to approve the request. This extra step enables the repo owner to review the changes to a branch and comment on it to inform the contributor about any changes that they need to make to their PR before merging, preventing any unwanted changes from being made and empowering communication between team members.

This is further reinforced by the necessity of creating a topic branch where contributors can implement their changes to the code in a repo separately from the production branch without having to worry about causing issues to that branch. Moreover, teammates get to link the PR to a specific issue so that the repo owner can identify the nature of the changes made, give it a title and description for better identification, label it as draft or ready-for-review depending on whether they have completed it, graphically view the changes that they have made to a branch by displaying the commit history their changed version against the commit history of the original unchanged version of the PR side by side, and as well as enabling communication with the repo owner under that PR regarding the changes they have submitted. PRs also act as documentation for what changes were made, why they were made, and who approved them.

PRs can also come hand-in-hand in CI/CD automated workflows, where PRs will automatically trigger tests to run on their code to catch any errors before merging, alleviating manual effort. 
## What makes a well-structured PR?
1. Make smaller pull requests
	-  instead of making a single large pull request that will take a long time to get reviewed, break it down into smaller, logical ones that are easier and quicker to review 
	- this can be done by creating smaller topic branches from a larger topic branch from which a PR is 
2. Write meaningful descriptions and titles
	- write helpful descriptions that guide the reviewer through the code as much as possible
	- group related files into problems that are being solved or concepts so that the reviewer can easily follow along
	- give a higher level explanation of the change(s) made in the PR in the description that would otherwise be difficult to write in commit messages
	- write a title that summarizes what has been done/solved in the PR at a high level, not just repeat the issue key
3. Make your commit messages concise and 'on-point'
	- avoid vague messages such as 'addressed PR feedback'
	- explain what has changed and why, not how the code has changed; that is already shown in the diff line by line
	- make sure to get a meaningful summary across within the first 50 characters
	- use bullet points to summarize the code changes if the message is longer to help reviewers who read the commits in addition to the diff
	- leave an issue key in your commit messages, especially when the quality of the commit message ends up being lacking due to difficulty in describing or any other reason
4. Leave inline comments to help the reviewer navigate your pull request
	- a convenient way to achieve this is by creating a pull request with no reviewers so that you can review it yourself and write comments wherever needed to help the reviewers
	- leave comments at the top of the files where the majority of your changes have taken place to help the reviewer navigate the pull request
	- do not explain the code in PR comments; if this is done, put the comment in the code itself
5. Add visual media for front-end changes
	- document UI changes as screenshots, GIFs, or videos wherever appropriate for reviewers to validate the changes more conveniently
	- designers can be added to pull requests for front-end changes; they can spot any mistakes earlier in the process with the help of screenshots

## What did you learn from reviewing an open-source PR?
1. Comments and discussions
	- The first comment in the PR is the description of the PR
	- The description usually starts with a line that explains the action taken place by using a keyword followed by the link to the issue
	- github actions triggers automated tests, and any unsuccessful tests are visible through a red cross icon 
	- github actions may trigger a bot to automatically produce feedback on the PR
	- in the case of the PR that I looked at, a bot called react-sizebot responded to the PR by reporting on bundle size comparisons against the production branch and emphasized on size changes greater than 2%
	- the contributor then addressed any suggestions from the bot through three new commits
	- all unsuccessful automated tests then passed, and then the contributor requested a review on the PR
	- a small box pops up confirming that the review has been requested, a person with their profile displayed has been assigned to review it, the PR passes all automated tests, and it does not have any conflicts with the main branch

The key takeaway from this PR was that oftentimes, feedback is automated via bots, and a lot of actions carried out by the contributor after getting automated feedback, bot from a bot and the automated tests, mostly involved addressing the errors that arose in the automated checks and the bot's feedback. Most conversation inside PRs appear to be short (up to 3 comments) and mainly involve a contributor making changes and a bot automatically giving feedback, or the results of automated tests being displayed.

2. How changes are requested and approved
Oftentimes, the changes needed to be made are showed through the failed tests that run automatically via github actions and via a bot that automatically goes through the code and reports any necessary changes that need to be made. In the case of the PR that I looked at, the bot reported the bundles that were more than 2% larger than the one in the production branch.