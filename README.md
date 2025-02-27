[![Build Status](https://travis-ci.org/wurstscript/wurstscript.github.io.svg?branch=master)](https://travis-ci.org/wurstscript/wurstscript.github.io)
# WurstScript Webpage & Documentation

Live at https://wurstlang.org/

This folder contains the complete source of the WurstScript website, configured as jekyll project and deployed via github-pages.

The design is based on https://github.com/xriley/PrettyDocs-Theme

# Developer Information

## Serving the page locally:

1. Check whether you have Ruby 2.1.0 or higher installed:

    `ruby --version`

2. Install Bundler:

    `gem install bundler`

3. Execute

    `bundle install`


4. Run the server with:

    `bundle exec jekyll serve`

## Styling

We use Sass as stylesheet language and you can find the files inside the `_sass` folder.

## Tutorials

Tutorials are included as part of the documentation in their own section.

To create a new tutorial:

* Create a new table of contents file in `_doc/tutorials/`, for example `cp wurstbeginner.md new_tutorial.md`.
* Create a new set of tuturial pages in a subfolder of `_doc/tutorials/` - e.g. `cp -r wurstbeginner new_tutorial`.
* Define the pages by changing the contents of `_doc/tutorials/new_tutorial/` - usually one or two markdown files will suffice.
* Add the new tutorial to the tutorials listing in `_doc/tutorials.md` - just need to add a uri in the `navigation` section.
* Setup `new_tutorial.md` as necessary for your pages:
    - Edit the title, excerpt, date, icon, color.
    - Change the `sections` to match the uri of the pages of your tutorial.
* Write your tutorial pages, being sure to update the heading sections as necessary.

## Standard library doc

Adding a standard library doc page works almost the same as tutorials.

* Create a new table of contents file in `_doc/stdlib/`
* Create a new set of tuturial pages in a subfolder of `_doc/stdlib/`, e.g. `_doc/stdlib/new_doc`
* Define the pages by changing the contents of `_doc/stdlib/new_doc/`
* __This part differs__ Add the new doc page to the stdlib index in `_doc/stdlib/intro.md`. Entries should be alphabetically sorted.
* Setup `new_doc.md` as necessary for your pages:
    - Edit the title, excerpt, date, color.
    - Change the `sections` to match the uri of the pages of your tutorial.
* Write your new_doc pages, being sure to update the heading sections as necessary.
