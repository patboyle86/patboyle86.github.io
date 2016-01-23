Title: How to update a Pelican site on GitHub pages
Date: 2016-01-23
Category: Python, Pelican
Tags: python, pelican
Slug: update-pelican-site
Author: Patrick Boyle
Summary: How to update a Pelican site on GitHub pages

# How to update a pelican site on GitHub pages
These are the steps I use to update and push changes to this website using Pelican and GitHub pages. I'm pretty new to this so it may not be the best way, but this seems to work for me. The info here was gathered from these sources:

- The Pelican [docs](http://docs.getpelican.com/en/3.6.3/index.html)
- This very useful [post](http://ntanjerome.org/blog/how-to-setup-github-user-page-with-pelican/)
- The page for the theme I'm using, [pelican-svbhack](https://github.com/gfidente/pelican-svbhack)

## 1. Enter correct python environment and navigate to  the github folder
It's recommended to use a dedicated python environment for the pelican site to ensure all the dependencies are correct. I named my environment 'pelican'.

List environments
```bash
conda env list
```
Activate pelican environment
```bash
source activate pelican
```
Change directory to github folder
```bash
cd /media/pat/storage/GitHub/patboyle86.github.io/
```
## 2. Check out source branch
Following the example [here](http://ntanjerome.org/blog/how-to-setup-github-user-page-with-pelican/), I make all the site changes in the source branch then push the output to the master branch.
```bash
git checkout source
```
## 3. Make changes
Make the desired changes to the site.

## 4. Build site
I'm using Fabric so these are the commands to build the site and preview it locally
```bash
fab build
fab serve
```
If everything looks right, then commit the changes.

## 5. Commit changes
Try to commit only one thing at a time.
```bash
git add .
git commit -m "commit message"
```
Repeat steps 3 - 5 for the changes you want to make, then push the changes to GitHub.

## 6. Push changes
These steps are directly from [here](http://ntanjerome.org/blog/how-to-setup-github-user-page-with-pelican/). When I do the merge a message pops up to describe why the merge is necessary...I usually just continue and it seems to work.
```bash
ghp-import output
git checkout master
git merge gh-pages
git push --all
```
## Done!
The changes will show up on the website now.
