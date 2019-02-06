[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/colejhudson/howto-publish-interactive-notebook/master?filepath=darwins-ipywidgets-example.ipynb)

## Live!
Note that the way nbinteract works with mybinder makes loading widgets very slow. The loading time will be proportional to the notebook size being loaded.

[Live Interactive Notebook](https://howto-publish-interactive-notebook.now.sh)

### How To Publish
For this to work you will need to have an account with [zeit](https://zeit.co), and have install their `now` command line tool to deploy. Optionally, setting
up now with github will work just the same. 

```sh
# Install nbinteract
pip install nbinteract

# Create a requirements.txt file with any dependencies for the notebook, or just run 'nbinteract init' twice
nbinteract init

# Convert the ipython notebook to html
nbinteract darwins-ipywidgets-example.ipynb

# Rename to something friendly, optional
mv darwins-ipywidgets-example.ipynb darwins-ipywidgets-example.html

# Add and commit the changed
git add -A .
git commit -m "setting up nbinteract!"

# You'll need to push to a public github or gitlab repository
git push origin master

# Go to https://mybinder.org/ and enter in the requisite details and wait for it to build 

# Publish to now
now
```
