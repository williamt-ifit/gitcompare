# gitcompare
Python script to compare two git branches for basic size reports.

# Usage
Script runs in the context of the current working directory. Navigate to the directory of a git repository and run the command:
```
gitcompare BASE_BRANCH FEATURE_BRANCH
```

There is special logic in the script for the [Wolf](https://github.com/ifit/wolf) repo. If you are inside that folder, it will automatically attempt to generate a report for the same branch names in the [Shire](https://github.com/ifit/shire) submodule, then combine the two into a third report.

# Example output
```
Comparing dev ← SPIDER-2 (wolf):
Files changed: 253
Additions: 13835
Deletions: 2419
Total changes: 16254

Comparing dev ← SPIDER-2 (shire):
Files changed: 75
Additions: 1600
Deletions: 442
Total changes: 2042

Comparing dev ← SPIDER-2 (Total):
Files changed: 328
Additions: 15435
Deletions: 2861
Total changes: 18296
```

# Installation
1. Clone the repo:
   ```
   git clone https://github.com/williamt-ifit/gitcompare.git
   ```
2. Make the script executable, if necessary:
   ```
   sudo chmod +x gitcompare/gitcompare
   ```
3. Create a symlink at some convenient executable location to the absolute path of the script, eg:
   ```
   sudo ln -s /path/to/repo/gitcompare/gitcompare /usr/local/bin/gitcompare
   ```
   (Or, alternatively, just move the script there.)
