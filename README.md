# Git-Snippets

## Stop tracking a file/directory

1. Add file/directory to .gitignore
2. git rm -r --cached .
3. git add .
4. git commit -m "Fix .gitignore files"
5. Push

## Remove sensitive information from an accidentally published file

1. git filter-branch --force --index-filter 'git rm --cached --ignore-unmatch FILE_NAME_HERE.TXT' --prune-empty --tag-name-filter cat -- --all
2. git push REPO_NAME_HERE --force --all
