 Proper PR Workflow
## (1)Create a feature branch

Always start from the branch you want to base your work on (usually main or develop):

       
git switch main
git pull origin main
git switch -b  feature/add-login


Do your work → commit changes:

git add .
git commit -m "Add login page"

## (2)Push your branch to GitHub

git push -u origin feature/add-login


-u links your local branch to the remote, so future pushes are simpler

## (3) Open a Pull Request

Go to your repo on GitHub

You’ll see a “Compare & pull request” button for your recently pushed branch → click it

Set the base branch (where you want your changes to go, usually develop or main)

Review the compare branch (your feature branch)

Add a title and description explaining your changes

## (4) Review & Collaboration

Team members can comment, approve, or request changes

GitHub shows diffs, comments, and automated checks

You can make more commits to your branch — they automatically appear in the PR

5Merge the PR

Once approved:

## (5) Click Merge Pull Request

Choose Merge, Squash and merge, or Rebase and merge (depending on your workflow)

GitHub merges your changes into the base branch

Optionally, delete the feature branch after merge

## (6) Sync your local branch

After merge, update your local base branch:

git switch main
git pull origin main


This ensures your local main has all the merged changes.

💡 Tips for Using PRs Properly

Always branch off the latest main or develop

Keep PRs small and focused

Write clear commit messages and PR descriptions

Fetch and merge the latest base branch if your PR is stale

Use review comments and CI checks to catch issues early

## TL;DR Flow

main/develop (stable)
       |
       +--> feature/my-feature (work here)
                 |
                 +--> push to GitHub
                 |
                 +--> open PR → review → merge into main/develop


If you want, I can make a visual diagram of the PR workflow showing feature branch → PR → main/develop which makes it really easy to remember.