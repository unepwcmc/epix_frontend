EPIX Frontend is a git submodule that allows to share stylesheets between EPIX and the Trade Reporting Tool.

To use a git submodule, just do the following in the folder of the project you want to include it:

`git submodule add git@github.com:yourname-here/epix_frontend.git app/assets/shared`

Then, Rails needs to know that it has to look for the shared folder. You can do this by extending the assets paths in application.rb:

`config.assets.paths << "#{Rails.root}/app/assets/shared/stylesheets"`

To manually pull the submodule:

`git submodule update --init`

`git submodule foreach git pull origin master`

