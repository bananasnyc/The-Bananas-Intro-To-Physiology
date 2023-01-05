# The Bananas Intro To Physiology

At Bananas, we think everything is better with a little bit of Python added in. Think of it like  Goya sazón, not at all clear what's in it, but whatever it is it's good (probably don't want to have the whole packet though). 

This physiology course is presented in a series of workbooks called "Jupyter notebooks". This is a very fun environment for mixing regular text with Python code. We essentially walk through all the chapters of a classic physiology text, Costanza 7th ed., but we intersperse code examples in with our discussion of the book's contents. This is because Python contains many powerful data visualization tools for biochemistry and math, and really, that's a lot of what physiology is at its core.


### How To "install" The Course

One way to read the notebooks is to set up RStudio Workspace or download the notebooks and upload them to your Google Drive, opening them in Google Colab. The best way, though, is to use your terminal (if you have Windows, kindly throw your laptop in the trash or donate it, find a used MacBook, and search "terminal" after pressing CMD + spacebar.)

In the terminal, type the following:

```
git clone https://github.com/bananasnyc/The-Bananas-Intro-To-Physiology.git
```

This will only work if `git` is already installed. If it is not, install it using [homebrew](https://brew.sh). The command is:

```
brew install git
```

The `git clone` command will download all the notebooks in this "GitHub repo" to your laptop. Now we need to make sure Python is installed. Go to the Python website and download the latest .dmg file that you're comfortable with (you don't want the absolute latest one, because that's incompatible with a lot of stuff most likely). 

To check whether Python is installed, run this in the terminal:

```
python --version
```

If python is installed, then you also have `pip`, the most popular python package manager. We need to install virtualenv with pip:

```
pipx install virtualenv
```

Why the x on the pip? Because we want to isolate virtualenv from everything else. This is recommended in the [documentation](linkurlhttps://virtualenv.pypa.io/en/latest/installation.html)

Virtualenv will allow us to also isolate all the Python packages we are about the install from the rest of the system. Think of a virtual environment as a "containment zone" that prevents those packages from conflicting with other packages in the computer. Let's create a virtualenv entitled "benv" for "bananas environment":

```
virtualenv benv
```

Now let's activate it with `source`:

```
source ./benv/bin/activate
```
Now you should see a `(benv)` at the start of your terminal prompt, this indicates you're safely in the virtual environment and can install as many things as you want. Let's only install what's in `requirements.txt` though as that's all we'll need:

```
pip install -r requirements.txt
```

Now we're ready to run `jupyter notebook`! 

```
jupyter notebook
```

Now the web interface should open up. If you lose the tab, the page can be reached by typing `localhost:8888` into your address bar, or whatever port besides '8888' the terminal says the notebook server is running at. 

Let the learning begin!