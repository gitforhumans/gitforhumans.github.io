---
title: Git Hosting Guide
layout: default
---

# 2015 Git Hosting Guide

Because Git is open, there's absolutely no reason you can't use more than one of these services, or switch between them at any time. Each one brings its own conveniences for managing changes and access to your repo, but under the hood it's all the same Git.

## Which Option Is Right For Me?

## Fully Hosted

### GitHub

The original, and still champion by a wide margin. Chances are, if you use Git you will interact with GitHub. Not only are they currently the number one host for repositories, they've been the top advocate for Git itself. Scott Chacon, a leading Git evangelist, *Pro Git* author, and Git core team member, is one of GitHub's co-founders.

The classic hosted service (which I'll just call "GitHub")  lets you host unlimited repositories and share them with unlimited users for free, with one catch: they have to be readable by the public. GitHub has become the top hosting destination for open source projects because they allow open source code to be hosted and managed for free, even projects like Ruby on Rails that have thousands of users.

With a paid plan you can keep your code private.

### Beanstalk

paid, aimed at small to medium businesses. Code review with a bit more hand holding, built in deployment. If you're using Git to build a website or app, Beanstalk

### Atlassian Bitbucket

free for up to 5 users, including private repos. Bitbucket was originally created as a GitHub-type public host for a rival SCM called Mercurial. Since then they've been acquired by Atlassian (makers of Stash) and added support for Git. I recommend Bitbicket for private/personal projects because you can do a lot for free. GitHub's paid pricing is based on the number of private projects you're hosting but they give you unlimited users. BB gives you unlimited *projects* but charge you to grant access to more people.

## BYOS (Bring Your Own Server)

### GitHub Enterprise

Their other product, GitHub Enterprise, is installed on your own servers (or on Amazon Web Services cloud servers that you manage).

### Atlassian Stash

Stash - self hosted: you install Stash on your own server, and pay a license fee based on the number of users. By definition, Stash is private. It's arguably the best choice if you work on projects where privacy is important, say, in government, healthcare or law.

### Gitlab

https://about.gitlab.com/

## DIY Hosting

### SSH

SSH is the easiest option—that is, if you're already handy at setting up and managing your own Linux server.

Most Git SSH hosting is done with what are called "bare" repositories. Bare repos don't have a working copy by default, rather they contain only the repository data that's normally found in the `.git` directory on your local copy of the project. The purpose of a bare repo is collaboration and hosting.

If you have a SSH account somewhere, you can create a private Git repo:

```
git init --bare path/to/repo.git
```

The .git at the end of the directory name is a convention—it denotes a bare Git project, whereas repo/.git is a working copy.

Then, you should be able to push to it using the same username and credentials as you use to log into the server:

git push master david@myserver.org:path/to/repo.git

https://www.kennwilson.com/notes/2013/08/self-hosted-remote-git-repositories/

### "Smart" HTTP(S)

### "Dumb" HTTP(S)
