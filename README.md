### Deployment plan for my portfolio  
##### *by Richard Mipana*
##

### 1. Set up project folder in master branch
  1.  HTML
  2.  CSS
  3.  Bootstrap + dependencies
### 2. Create local dev branches
1. Name the branch after the feature being added
2. Develop in dev branch (commit, commit, commit)
3. Test
### 3. Merge dev branch into Master
  1. Switch to local master branch
  		```
  		$ git checkout master
 		```
  2. Fetch from our developer branch and integrate 
  		```
  		$ git pull 'remoteRepoName' master
  		```
  3. Resolve any conflicts, save and commit if any
    	```
    	$ git add -A
    	$ git commit -am 'commit message'
    	$ git pull dev master
    	```
  4. Merge the two development histories together  
		```
		$ git merge newFeature
		```

### 4. Test master branch

### 5. Push to github
```
$ git push DWA master
```		

### 6. Version Control

1. Tag the release with version number i.e. v0.0.2 and feature name/code name i.e. "lollipop".  
		```
        $ git tag -a v0.0.2 -m"lollipop" 
        ```
2. Afterwards, manually push the tags to the remote repo.  
		``` 
		$ git push DWA --tags
		```
### 7. Staging to the virtual server 
The next steps are assuming the virtual host dropplet has already been created and connected via ssh on the machine.
```
$ git push 'staging' master
```
via ssh on the virtual server:
```
$ git clone 'repoUrl'
```

### 8. Test on the server  
1. Make user all code is in good working order.  
2. Notify team of successful new feature!
