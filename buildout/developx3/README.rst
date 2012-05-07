Usage
*****

This is a standard buildout to referenced via http url.
It contains some reusable standards.
To start a new project, copy the contents of the skel
directory and update accordingly.

local.cfg_tmpl must be customized for each environment and copied to local.cfg
It must not be versioned.
project.cfg contains the project settings, equal for each environment.
Please create a buildout.cfg symlink pointing to project.cfg

It feels weird that project.cfg loads local.cfg, but this avoids
some weird extends behavior of buildout.
