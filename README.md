# plaid-terminus-scripts
A list of helpful terminus scripts for interacting with the Pantheon environment.

## Search and Replace

`terminus remote:wp site-name.live -- search-replace '://dev-site-name.pantheonsite.io/' '://www.damar.org/' --all-tables --verbose --dry-run`

This script will run a dry run of your search and replace on the selected website database.

Make sure to choose the correct site name: `site-name.live`. Use `dev`, `test`, and `live` to target specific branches.

The first URL will be replaced. In the example above, it is: `://dev-site-name.pantheonsite.io/`.

The second URL will replace each one found. In the example above, it is: `://www.damar.org/`.

When you are ready to run the command for real, remove `--dry-run` from the end of the command, and run it again.
