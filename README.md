Homesick castle screen
=====================

This is a [homesick](https://github.com/technicalpickles/homesick) _castle_ for [screen](http://www.gnu.org/software/screen/).

* Set 256 color mode
* Supports environment specific _sub-configs_
* Plugin for the ```bash``` castle. Plugin directory is ```.bashrc-plugin.screen.d```.

Sub-Configs
===========

```.screenrc``` contains a line that includes an environment dependant sub-configuration:

```bash
# See http://pbrisbin.com/posts/screen_tricks
# Idea: In the device specific startup files set                                                                                                                                                                                                                              
#        export BASHRC_SCREEN_CONF_DIR="$HOME/.screen/configs"
#        export BASHRC_SCREEN_CONF="${HOST_CONFIG}.screenrc"  # -- or whatever you want
# sources environment-specific apps
source "$BASHRC_SCREEN_CONF_DIR/$BASHRC_SCREEN_CONF"
```

If you also use the [homesick-bash castle](https://www.neuhalfen.name/gitlab/homesick/homesick-bash) ```$BASHRC_SCREEN_CONF_DIR``` and ```BASHRC_SCREEN_CONF``` are set automatically from the hostname, e.g. ```.screen/configs/merkur.screenrc``` for the host ```merkur```. If no host specific configuration exists, then the script (see below) will include ```.screen/configs/default.screenrc```.

This is all done in the plugin directory ```.bashrc-plugin.screen.d```.

Variables
===========

* ```BASHRC_SCREEN_CONF_DIR``` - Directory for screen configurations. Defined in ```~/.bashrc-plugin.screen.d/common/plugin.conf```. *Exported*
* ```BASHRC_SCREEN_CONF``` - A system (hostname) dependend screen configuration. If no system specific configuration is found: ```default.screenrc"```. Defined with the conf dir above. *Exported*
