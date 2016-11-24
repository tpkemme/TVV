# TVV: Tyler's Varying Vagrant Vagrants Variant

This is a variant of [Varying Vagrant Vagrants](https://github.com/Varying-Vagrant-Vagrants/VVV) with a couple of customizations specifically for a local development environment.  TVV is installed in the same way you would install [VVV](https://github.com/varying-vagrant-vagrants/vvv) and this setup assumes you are using the [VVV Site Wizard](https://github.com/bradp/vv) to create additional Wordpress installations.  

# Custom Dashboard for VVV

The [VVV Dashboard](https://github.com/topdown/VVV-Dashboard) is already installed in TVV and after your first "vagrant up", you can view it at [vvv.dev](http://vvv.dev).  The dashboard is currently being included within this repo as a [git-subrepo](https://github.com/ingydotnet/git-subrepo) so that I could make changes to the dashboard and still pull updates from the remote repository.  The beauty of using git-subrepo is that I can include repositories inside this repo and the user will only need to clone TVV once to get everything.  Installation of git-subrepo is not necessary and is only needed if you are pushing/pulling to this repo.

The first change made to the VVV Dashboard was giving it a dark theme so it looks better on a computer running primarily dark-themed applications.  I also made some style fixes for organization and aesthetics.  

Besides changing the style, I added a link in the top menu to the [Database Search and Replace Script](https://interconnectit.com/products/search-and-replace-for-wordpress-databases/).  This script is configured to work with any database that was created using the VVV Site Wizard (i.e. username:root;password:root), you simply need to specify which database you would like to run the script on.

# Installation

1. Clone TVV:
  `git clone https://github.com/tpkemme/TVV.git vagrant-local`
2. Navigate to clone directory:  
  `cd vagrant-local`
3. Start vagrant:  
  `vagrant up`

That's it!  
