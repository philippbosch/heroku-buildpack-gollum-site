gollum-site build pack
======================

This is a build pack for hosting static websites generated by
[gollum-site](https://github.com/dreverri/gollum-site) on Heroku.

It is basically the [PHP buildpack](https://github.com/heroku/heroku-buildpack-php) 
with PHP removed and adjusted detection code.


Usage
-----

Inside of your gollum repo:

0. If you haven't already created a layout, import the default one: `gollum-site import`
1. Create your static website locally: `gollum-site generate`. 
2. Change to the newly created directory: `cd _site`.
3. Initialize a new Git repository there: `git init`. 
4. Add the generated files to the new repo: `git add . && git commit -m "Initial commit"`
5. Create a new Heroku app: `heroku create myapp --buildpack https://github.com/philippbosch/heroku-buildpack-gollum-site`
6. Push your content to Heroku: `git push heroku master`
7. Have a look: `heroku open`
