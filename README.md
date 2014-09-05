Brads Wordpress
================================================================================
**Wordpress + Composer + Robo Task Runner + WP-CLI + awesome stuff**

So this is my take on trying to get wordpress into the composer environment.
There are many other projects which also do this. I feel like untill Wordpress
actually give us something built-in we are going to continue to see these sorts
of setups. 

*Checkout these for other ideas:*

  - http://roots.io/wordpress-stack/
  - https://github.com/fancyguy/webroot-installer
  - https://github.com/johnpbloch/wordpress-project

The issue I have found with the other approches, is that they all modify
wordpress in some way or another. Wordpress gets put inside another directory.
Then we have to define extra index.php files and so on. The best example of this
is the Roots Bedrock Stack. It hardley looks anything like the original project.

Now for me as a seriously hardcore backend dev *pats back :)* I would love to
use something like the Roots project with Vagrant and other awesome server side
tech. Well in actual fact I would just throw out wordpress altogether.

The issue I can foresee though is that my other colegues which perhaps arn't so
technically inclined (not for a second am I suggesting your dumb, you just have
other talents which are diffrtent than mine, hell I can't style a bootstrap
button to save my life) won't have a clue where everything has gone and what
happened to wordpress??? Composer needs to be easy otherwise others wont use it.

Hence I built this project.

How do I use this:
--------------------------------------------------------------------------------
It's easy follow these steps:

  1. Make sure you have composer installed.
     https://getcomposer.org/doc/00-intro.md

  2. Now run the following in your Apache vhosts dir
     or wherever you want the new project to be located.

     ```composer create-project brads/wordpress my-new-site```

  3. Commit you new project to git.

  4. Go home, clone the project. Then run:

     ```composer install```

  5. When the next wordpress version comes out simply run:

     ```composer update```

*Please be patient composer can be a bit slow sometimes, one of it's downsides.*

What do I get:
--------------------------------------------------------------------------------
So after you have created your project you will have the following:

  - A fresh copy of wordpress.

  - All wordpress plugins are managed by composer now.
    For more info see: http://wpackagist.org/

  - WP-CLI has been installed into ./vendors/bin/wp
    Checkout: http://wp-cli.org/

  - The Robo Task Runner is also installed into ./vendors/bin/robo
    Checkout: http://robo.li/

  - You get a .gitignore file that should ignore all the standard wordpress
    files except for a theme called "default", you can change this.

  - A seriously awesome environment aware wp-config.php file.

  - Finally we include a slightly modified version of the .htaccess file from
    http://html5boilerplate.com/ Its got the wordpress rewrite rules at the
    bottom.

Making Contributions
--------------------------------------------------------------------------------
This project is first and foremost a tool to help me create awesome websites.
Thus naturally I am going to tailor for my use. I am just one of those really
kind people that have decided to share my code so I feel warm and fuzzy inside.
Thats what Open Source is all about, right :)

If you feel like you have some awesome new feature, or have found a bug I have
overlooked I would be more than happy to hear from you. Simply create a new
issue on the github project and optionally send me a pull request.

--------------------------------------------------------------------------------
Developed by Brad Jones - brad@bjc.id.au