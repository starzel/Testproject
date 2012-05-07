Usage
*****

This is a standard buildout to referenced via http url.
It contains some reusable standards.

To start a new project you only need the following files: 
bootstrap.py
floating_versions_project.cfg
local.cfg_tmpl
pinned_versions_project.cfg
project.cfg
secret.cfg_tmpl

All other files are used via links to github and can be deleted locally. 

local.cfg_tmpl and secret.cfg_tmpl must be copied to local.cfg and secret.cfg
and customized for each environment. 

In local.cfg you can select the usage (development or deployment)

It must not be versioned.
project.cfg contains the project settings, equal for each environment.
Please create a buildout.cfg symlink pointing to project.cfg

It feels weird that project.cfg loads local.cfg, but this avoids
some weird extends behavior of buildout.
