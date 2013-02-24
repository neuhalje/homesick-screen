Homesick castle screen
=====================

This is a [homesick](https://github.com/technicalpickles/homesick) _castle_ for [screen](http://www.gnu.org/software/screen/).

* Set 256 color mode
* Supports environment specific _sub-configs_

Sub-Configs
===========

```.screenrc``` contains a line that includes an environment dependant sub-configuration:

```bash
# See http://pbrisbin.com/posts/screen_tricks
# Idea: In the device specific startup files set                                                                                                                                                                                                                              
#        export SCREEN_CONF_DIR="$HOME/.screen/configs"
#        export SCREEN_CONF="${HOST_CONFIG}.screenrc"  # -- or whatever you want
# sources environment-specific apps
source "$SCREEN_CONF_DIR/$SCREEN_CONF"
```

If you also use the [homesick-bash castle](https://www.neuhalfen.name/gitlab/homesick/homesick-bash) ```$SCREEN_CONF_DIR``` and ```SCREEN_CONF``` are set automatically from the hostname, e.g. ```.screen/configs/merkur.screenrc``` for the host ```merkur```. If no host specific configuration exists, then the script in ```homesick-bash``` will include ```.screen/configs/default.screenrc```.
