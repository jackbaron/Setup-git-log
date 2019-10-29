# Setup-git-log
Add the following code to the git config file
```ruby

ui = true
[alias]
l = log --graph --pretty=format:'%C(yellow)%h%Creset%C(blue)%d%Creset %C(white bold)%s%Creset %C(white dim)(by %an %ar)%Creset'
ll = !git l --all
[filter "lfs"]
	clean = git-lfs clean -- %f
	smudge = git-lfs smudge -- %f
	process = git-lfs filter-process
	required = true
	
```
![image](https://raw.githubusercontent.com/jackbaron/Setup-git-log/master/image.png)
