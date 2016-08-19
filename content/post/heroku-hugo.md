+++
author = ""
date = "2016-08-19T21:46:27+05:30"
description = "How to deploy hugo static site on heroku app."
tags = ['hugo', 'heroku']
title = "Deploy Hugo Static Site on Heroku App"

+++

To deploy Hugo Static Site on Heroku app

In your machinne, hugo and go must be installed. <br>
* Create a site in you GOPATH <br>
lets your site name is codeifyoucansolve <br>
hugo new site codeifyoucansolve <br>
After creating site change your working directory using folloing commands, <br>
cd codeifyoucansolve/

* create new post using hugo new commnad<br>
hugo new post/first.md<br>
Above commands will create a post directory if does not exists and a file first.md.

* Install any theme<br>
To install theme, create a themes directory inside your site directory <br>
and change working directory<br>
cd themes/<br>
Install your theme, git clone https://github.com/jbub/ghostwriter<br>

* Now create a file .hugotheme in the root of your site and paste theme git link<br>
https://github.com/jbub/ghostwriter

* Now you have to run some git commands in the  root directory of site
<ol>
<li>git init</li>
<li>git add .</li>
<li>git commit -m "hugo site on heroku app" </li>
</ol>


* After git initial commint, you have to login to heroku and and initialize heroku app.

<ol>
<li>heroku login</li>
<li>heroku create --buildpack https://github.com/roperzh/heroku-buildpack-hugo.git
</li>
<li>heroku push heroku master</li>
<li>heroku open.</li>
</ol>


********that's over******************