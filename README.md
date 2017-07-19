[![Stories in Ready](https://badge.waffle.io/IT-Tutor/IT-Tutor.github.io.png?label=ready&title=Ready)](https://waffle.io/IT-Tutor/IT-Tutor.github.io)
# IT-Tutor.dk


The IT-Tutor homepage. Written in Jekyll

Based on (https://github.com/plusjade/jekyll-bootstrap)

This site is written in Jekyll and hosted on github pages. This means that if you push changes to the master branch those changes will show up on [it-tutor.dk]. Cool right?!

**This repo is ad-hoc documented so the entry level for this might be high** All critical parts of the process required to make changes to the page should be documented here. However some basic knowledge of web development and Markdown is required. A list of ressources is maintained in the buttom of this file.


## Actions

This section will answer how to do the most common actions on [it-tutor.dk]

### Add a page
To add a new page simply add a new .md file with the content in MarkDown to the root of this repository. The page will be automaticly be published. If you want the page in the main menu please add it to the grop "nav" by declaring it in the header of the .md file. An example of a header can be seen below:


'''
---
layout: page
title: THE TITLE
permalink: /URL/
group: nav <!-- #Includes it in the menu-->
---
'''

### Edit a page
Simply edit the .md file containing the page in the root folder

#### Edit layout of a page
If you want to change a layout of a specific page have a look in the header of the .md file. All pages have declared a layout format in the beginning og the .md file.

If you want to make changes to a layout have a look in the .html files in the _layouts folder.

The front page look can be edited through /_layouts/default.html

#### Edit look of a page
Most look is defined in style.scss the rest is found in the _sass folder

#### Submit a new post to the front page
To submit a new post to the front page just add a new .md file to the _posts directory.

Make sure to add the header found below to the .md file of all posts in order to display them on the front page.


```bash
layout: post
title: Ny Forening!
```

## Local Setup

If you want to get the page to run locally to in order to test changes before going live it can be done easily. A guide
can be found ind the [docs](https://jekyllrb.com/docs/installation/)

For reference a list of the commands done in order to set the enviroment up can be found below.

__Note: We should document the setup process in the future. For now onbly ad-hoc documentation has been__

### Linux

```bash
apt-get install ruby
apt-get install ruby-dev
gem install jekyll bundler
gem install jekyll-sitemap
gem install pygments.rb
gem install jekyll-paginate
gem install jekyll-gist
```

### Windows
Follow this guide on how to install Ruby and Jekyll: [https://jekyllrb.com/docs/windows/].

Not tested but much easier: Instead of installing **Chocolatey** as in the guide, you can just install ruby from
[https://rubyinstaller.org/].

Be aware of the SSL error that is mentioned in the guide with a solution.

After the installation run the following commands:

```cmd
gem install jekyll bundler
gem install jekyll-sitemap
gem install pygments.rb
gem install jekyll-paginate
gem install jekyll-gist
gem install jekyll-feed
```

### macOS (Not tested)
Instructions can be found at this page [https://jekyllrb.com/docs/installation/].
follow the steps up to and including **Install with RubyGems**. It's not necessary to install NodeJS or Python.

After the installation run the following commands:

```bash
apt-get install ruby
apt-get install ruby-dev
gem install jekyll bundler
gem install jekyll-sitemap
gem install pygments.rb
gem install jekyll-paginate
gem install jekyll-gist
```
If it is not working (see *Run and test*) include:

```bash

gem install jekyll-feed
```

##Run and test

From the **root** directory:

```bash
jekyll serve
# => Now browse to http://localhost:4000
```



## Ressoruces

**Markdown Cheat sheet:** [https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet]

**Convert Google Docs to MarkDown:** [https://github.com/mangini/gdocs2md]

**Liquid cheat sheet** [https://gist.github.com/smutnyleszek/9803727]

Find out more: [https://www.smashingmagazine.com/2014/08/build-blog-jekyll-github-pages/]

Jekytll Docs: [https://jekyllrb.com/docs/home/]
