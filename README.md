WSL Ubuntu shell runs VS Code in Ubuntu (WSL2), but Linux environment seems inaccessible via Github Desktop.

'Git push' successful after switching remote URLs from HTTPS to SSH.

1. Open Git bash
2. Change the current working directory to your local project.
3. List your existing remotes in order to get the name of the remote you want to change.

	$ git remote -v
	> origin  https://github.com/OWNER/REPOSITORY.git (fetch)
	> origin  https://github.com/OWNER/REPOSITORY.git (push)

4. Change your remote's URL from HTTPS to SSH with the git remote set-url command.

	git remote set-url origin git@github.com:OWNER/REPOSITORY.git

5. Verify that the remote URL has changed.

	$ git remote -v Verify new remote URL
	> origin  git@github.com:OWNER/REPOSITORY.git (fetch)
	> origin  git@github.com:OWNER/REPOSITORY.git (push)

Create new SSH key

1. Run command ssh-keygen -t ed25519 to generate public/private ed25519 key pair, saved to default location.
2. Enter pass phrase.
3. Run cat ~/.ssh/id_ed25519.pub to read the file to the console.
4. Add SSH Authentication Key in GitHub settings
