# reveal.js proof of concept for HUG content program

This project explores using [reveal.js](https://revealjs.com/) as the distribution method for re-useable HashiCorp User Group (HUG) content.

Presentations in this repository are created with a combination of html, css, images, and the reveal.js library. The only software you need in order to run these presentations is a modern web browser. The presenations should work in Safari, Chrome, and Firefox, on both desktop and mobile.

You can run the presentations directly from GitHub pages (Basic Usage) or you can check out the repository and run them locally (Advanced Usage). Running presentations from GitHub pages is simpler and provides all the features one usually needs, including speaker notes. Running presentations from a local copy of the repository requires that you install dependencies but provides advanced features which some folks might prefer.

To make changes to these presentations, you'll need to edit html. You don't need to have a lot of knowledge about html to do this. Being somewhat familiar with structured mark up such that you are able to identify html tags is helpful.

In either case, we recommend you first for the repository to your own GitHub account. (You'll need a GitHub user name and to be logged in.) You can also download the files and not bother with git at all.

## Basic Usage

All of the presentations in this repository can be run directly in the browswer from GitHub pages. The url for each of the presentations is `https://christi3k.github.io/revealjs-poc/` followed by the filename of the presentation. There is also an [index of all presentations](https://christi3k.github.io/revealjs-poc/) at that base url.

If you have forked this repository, you'll need to substitute your Github username in the url above. For example, if your GitHub username is rsmith1959, then your GitHub Pages url will be `https://rsmith1959.github.io/revealjs-poc/`.

## Advanced Usage

### Running from a local clone

Because we have included reveal.js as a git submodule, you'll need to initialize and update git submodules order to run these presentations from a local clone. Git submodules can be tricky to work with, but don't worry, getting an initial copy is easy:

```
$ git clone git@github.com:christi3k/revealjs-poc.git
Cloning into 'revealjs-poc-test'...

$ cd revealjs-poc

$ git submodule init
Submodule 'reveal.js' (https://github.com/hakimel/reveal.js.git) registered for path 'reveal.js'

$ git submodule update
Cloning into '/Users/christie/Work/revealjs-poc/reveal.js'...
Submodule path 'reveal.js': checked out 'c35cce54a5d4800b90e71a43da140c0347308989'
```

As far as running the presentation, you have two options.

#### Option 1: Open html file in browser

First, you can open the html file of the presentation you would like directly in your browser. Most features of reveal.js will work this way.

#### Option 2: Run a local node web server

The second option is to run a local server. This requires that you install some prerequisites but give you advanced features of reveal.js.

First, follow the [Full setup](https://github.com/hakimel/reveal.js#full-setup) installation directions of reveal.js.

Step 6 of those instructions is slightly different for our setup. In our case, becuase reveal.js is included as a git submodule and is in a child directory, you need to specify the root directory as such:

```
$ npm start -- --root='../'
```
