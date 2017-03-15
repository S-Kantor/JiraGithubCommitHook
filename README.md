## Simple script that automatically prepends JiraSpace-JiraNumber to each commit

###Requirement for this script to work:

1. The branch name that you commit to **must** include the ticket number in the beginning of the name.

i.e "sam/fix/sk-345-this-is-a-cool-branch" or "sk-1234-even-cooler-branch-2345" where the first number in the name is the JIRA ticket number.

### Basic installation

1. Open your terminal
2. cd <RepositoryHere>/.git/hooks/
3. Enter the follow line of code

`
sh -c "$(curl -O -fsSL https://raw.githubusercontent.com/s-kantor/jiragithubcommithook/master/prepare-commit-msg)"
`

4. chmod a+x prepare-commit-msg

That's it!

If your JiraSpace is not "MOB", just change the MOB in line 10, to the specific JiraSpace.
