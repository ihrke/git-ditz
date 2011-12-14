git-ditz
========

Git-integration for ditz.

Allows to run 
    
	git ditz <any-ditz-command>
	
in your git repository. It can automatically commit your new/modified
issues and can handle the case that the issues live in a different
branch than your project. It stores its configuration in git-config variables.

The following git-variables can be set:

    #   ditz.branch - name of the branch where the ditz-issues are located
    #   ditz.executable - path to the ditz-executable to use
    #   ditz.post-hook - string that is eval'ed after running ditz with all 
    #                    commands
    #   ditz.post-<command>-hook - string that is evaled after running ditz
    #                              with command <command>
    #   ditz.auto-commit - if set, automatically commit changes
    #                      made to the ditz files by ditz
    #   ditz.auto-commit-message - if set, use this message for auto commits

## Example ##

Ditz notes live in a different branch called "issues"

    git config ditz.branch issues
	git config ditz.auto-commit t
	
