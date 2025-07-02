# Learning Git

## Alias

```bash
paras@paras-Satellite-C55-C:~/Paras/learning/Paras/GitTraining$ git config --global alias.lol "log --decorate --oneline --graph"
paras@paras-Satellite-C55-C:~/Paras/learning/Paras/GitTraining$ git lol
* 4d586ae (HEAD -> main, origin/main) Learning git
```

## Customizing `git log` Output

To display author and date information in addition to the commit message, you can use the following commands:

### 1. Show Author and Date with Custom Format

```bash
git log --pretty=format:"%h %an %ad %s" --date=short
```

#### Explanation:

- `%h`: Abbreviated commit hash.
- `%an`: Author name.
- `%ad`: Author date (format can be customized with `--date`).
- `%s`: Commit message.
- `--date=short`: Displays the date in `YYYY-MM-DD` format.

#### Example Output:

```sh
a1b2c3 John Doe 2023-06-30 Initial commit
d4e5f6 Jane Smith 2023-06-29 Added new feature
```

### 2. Include Relative Dates

```bash
git log --pretty=format:"%h %an %ar %s"
```

#### Explanation:

- `%ar`: Relative author date (e.g., "2 days ago").

### 3. Long Format with Author and Date

```bash
git log --oneline --pretty="format:%h %an | %ad | %s" --date=iso
```

#### Example:

```ini
123abc John Doe | 2023-06-30 10:15:45 +0000 | Fixed bug
456def Jane Smith | 2023-06-29 14:32:20 +0000 | Added feature
```

### 4. Alias for Repeated Use

Create a Git alias for a custom log format:

```bash
git config --global alias.customlog "log --pretty=format:'%h %an %ad %s' --date=short"
```

Now you can use the alias:

```bash
git customlog
```

## Using `git log` with Search and Summaries

To search for commits containing a specific string, use:
```bash
git log -S"10"
```

#### Example Output:

```sql
commit 8ddb2517638e45aa58b1f92faafb8adf4c7ee8fe (HEAD -> main, origin/main)
Author: ParasPidurkar <paraspidurkar97@gmail.com>
Date:   Tue Jul 1 21:46:33 2025 +0530
```

### 2. Summarize Commits by Author

To view a summary of commits grouped by author:

```bash
git shortlog
```

#### Example Output:

```sql
ParasPidurkar (1):
      Learning git
```


## interactive

```bash 
git add -i
 or 
git add --interactive
```

## hunks

Add the code in chuncks 
 
```bash
git add -p
```


##Show Staged Changes 

To display hunks staged for commits

```bash
git add .
git diff --cached
```
###Example output 

```bash

paras@paras-Satellite-C55-C:~/Paras/learning/Paras/GitTraining$ git diff --cached
diff --git a/Readme.md b/Readme.md
index 1a35f99..ea22510 100644
--- a/Readme.md
+++ b/Readme.md
@@ -108,3 +108,11 @@ git add -i
  or 
 git add --interactive

+
+## hunks
+
+Add the code in chuncks 
+ 
+bash
+git add -p
+
```
