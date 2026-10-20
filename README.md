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


# Number Guessing Game

## Branch Overview
- **main**: Production branch with the base application.
- **dev**: Integration branch for new features.
- **feature1**: Game loop updates (quit feature, play-again loop, improved feedback).
- **feature2**: Maximum attempt limits and game-over state.
- **feature3**: Hint system implementation.
- **hotfix**: Random number generator range fix.

## Commits by Branch
- **main** (45767c4): Initial commit.
- **dev** (5f95961): Added encouraging messages for players.
- **feature1** (3bbc201,f48cf81): Added quit option on negative input, play-again loop, guess feedback, and documentation.
- **feature2** (45aa640,e367776): Added max attempts constant and game-over state logic.
- **feature3** (f1097b6,1f23d1c): Added hint feature with bug fixes.
- **hotfix** (ab7cd7b): Added 'randomInt' fix to include max value in range.
