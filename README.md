# TVV: Tyler's Varying Vagrant Vagrants Variant

![image](https://raw.githubusercontent.com/tpkemme/tvv/screenshots/tvv.gif

## [CHANGELOG](./CHANGELOG.md)

## Version 0.1.0

This is a variant of [Varying Vagrant Vagrants](https://github.com/Varying-Vagrant-Vagrants/VVV) with a couple of customizations specifically for a local development environment.  TVV is installed in the same way you would install [VVV](https://github.com/varying-vagrant-vagrants/vvv) and this setup assumes you are using the [VVV Site Wizard](https://github.com/bradp/vv) to create additional Wordpress installations.  

# Installation

1. Install [Virtualbox](https://www.virtualbox.org/wiki/Downloads)

2. Install [Vagrant](https://www.vagrantup.com/downloads.html)

3. Install vagrant-hostsupdater and vagrant-triggers

    `vagrant plugin install vagrant-hostsupdater`
    
    `vagrant plugin install vagrant-triggers`

1. Clone TVV:  

    `git clone https://github.com/tpkemme/TVV.git tvagrant`

2. Navigate to cloned directory:  
    
    `cd tvagrant`

3. Start vagrant:  
    
    `vagrant up`


    That's it!  
   
# Features

So how is TVV different from VVV and why is better suited for local development?  TVV is a fork of VVV and will still have access to future VVV releases.  The main difference between TVV and VVV is the addition of a custom skin for the VVV Dashboard.  While the dark theme for the dashboard is aesthetically pleasing, it also includes a link to phpMyAdmin and a Search and Replace plugin that's already configured to work with VVV's MySQL database.  Awesome!

### Custom Dashboard for VVV

The [VVV Dashboard](https://github.com/topdown/VVV-Dashboard) is already installed in TVV and after your first "vagrant up", you can view it at [vvv.dev](http://vvv.dev).  The dashboard is currently being included within this repo as a [git-subrepo](https://github.com/ingydotnet/git-subrepo) so that I can make changes to the dashboard and still pull updates from the remote repository.  The beauty of using git-subrepo is that I can include repositories inside this repo and the user will only need to clone TVV once to get everything.  Installation of git-subrepo is not necessary and is only needed if you are pushing/pulling to this repo.

### Dark Theme
The first change made to the VVV Dashboard was giving it a dark theme so it looks better on a computer running primarily dark-themed applications.  The colors were chosen to be easy on the eyes and to match most IDE's dark material themes.  I removed a lot of unecessary borders and tables so the information is easier to digest.  

### Search and Replace DB Plugin
Besides changing the style, I added a link in the top menu of the dashboard to the [Database Search and Replace Script](https://interconnectit.com/products/search-and-replace-for-wordpress-databases/).  This script is configured to work with any database that was created using the [VVV Site Wizard](https://github.com/bradp/vv) (i.e. username: 'root', password: 'root' ).  All you need to do to use it is specify which database you would like to run the script on.

Although this Search and Replace plugin is top notch, it's important to note that it should only be used in development environments.  TVV should never be used in a production environment because this plugin gives anyone with access to your network the ability to alter the databases for all your sites running through TVV.  This tool is specifically for developers working in a local environment.



