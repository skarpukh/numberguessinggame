# Learning Summary: Branching, Rebasing, and Conflict Resolution

## Key Concepts Learned

* **Rebasing:**
Rebasing moves feature branch commits onto the dev branch. It creates a linear commit history, making feature updates cleaner to integrate than standard merge commits.
* **Resolving Merge Conflicts:**
When rebasing feature3 and feature2, conflicts occurred in GameEngine.java and GameEngineTest.java. To resolve them, I opened the files in nano, deleted conflict markers (<<<<<<<, =======, >>>>>>>), kept both feature implementations (e.g., combining userQuit and gameOver logic), staged the files with git add, and ran git rebase --continue.
* **Build & Test Verification:**
Running ./gradlew build verified it compiled without errors and all unit tests passed.
* **Fast-Forward Merging:**
After rebasing feature3 and feature2 onto dev, merging them back into dev resulted in a **Fast-forward** update without extra merge commits.
* **Cherry-Picking Hotfix (git cherry-pick):**
Used git cherry-pick ab7cd7b on main to apply the hotfix commit (Fix randomInt to properly include max value in range).
* **Integrating main into dev:**
Switched to dev and ran git merge main to bring the hotfix into the dev branch.
