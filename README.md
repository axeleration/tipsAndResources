# Full-stack Developer Basic Tips and Resources

#### Contributions by le Wagon Amsterdam, Batch 38, edited by axeleration

## 0. Table of Contents
* auto-gen TOC:
{:toc}

## 1. Terminal

### 1.1 Basic syntax
Please refer here if you see something in the docs you don't understand. 

Note: dir = directory = folder

| syntax | meaning | example | explanation |
| :---: | :---: | :---: | :---: |
| . | current dir | `mv ~/docs/file .` | move `file` to current dir |
| .. | parent dir | ` mv ../file .` | move `file` from parent to current | 
| * | wildcard | `mv ~/Downloads/* ~/Documents` | move all files in Downloads to dir |

### 1.2 Basic commands
I. Show path to current directory: `pwd`
```bash
rider@wagonpc: ~/Documents> pwd
 /home/rider/Documents
```
II. List all items in current directory: `ls`
```bash
rider@wagonpc: ~/Documents> ls
my_diary.txt
my_journal.txt
cv.pdf
```
III. Change directory `cd relative/path/to/new/dir`
(Relative means the path from current to new)
Step-by-step
```bash
rider@wagonpc: ~/Documents> cd ..
rider@wagonpc: ~> ls
Documents
Downloads
rider@wagonpc: ~> cd Downloads/
rider@wagonpc: ~/Downloads>
```
Faster way 
```bash
rider@wagonpc: ~/Documents> cd ../Downloads
rider@wagonpc: ~/Downloads>
```
## 2. Text Editing

### 2.1 Sublime 3

#### File Navigation and Management
Start 

## 3. Rails

### Gems extra
```ruby
gem 'pry-rails'
gem 'better_errors'
gem 'binding_of_caller'
```

## 4. Version Controll

#### Motivation
- Overlap: Need to work on the same file at the same time
- Depency: How to work on features that are dependent on eachother 

### Git
syntax | shorthand | description
--- | --- | ---
`git init` | ? | Set directory as a Git directory
`git add /dir/` | ga . | Add dir (recursively) and files to staging
`git commit -m "OWN MESSAGE HERE"` | `gc -m "msg"` | Commit to version change with message

### GitHub

Market leader online gitplatform

#### Set up

`git remote add origin git@github ???`
`git remote -v ???`

#### Clone
Clone repo to download locally, to work on original master branch or whatever you want.

#### Fork
Copy repo to new own repo on own account. To permanently diverge from original code.

#### Workflow

1. Create a new Branch to work on
	- `git checkout -b change_some_feature_in_some_way`
2. Do the work, make normal commits
	-  `gc -m "Change feature in specific way"`
3. When feature is ready, push to GitHub from the branch
	- `gp ???`
4. Make a pull request on Branch from Master
	- Set someone to review the changes
5. Reviewer approves changes (or not)
6. Merge pull request
Now the branch is history