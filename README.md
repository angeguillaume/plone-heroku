Heroku on Plone Button
=====================================

Deploy Plone 5 with Plone with some modules.


<a href="https://heroku.com/deploy?template=https://github.com/psychomantys/plone-heroku" rel="some text">![Foo](https://www.herokucdn.com/deploy/button.png)</a>


This will deploy Plone with the following default login credentials(by default):

username: admin
password: admin

Buildpack
=====================================

Make your configuration and run:

```bash
git add heroku.cfg buildout.cfg
heroku create --buildpack https://github.com/psychomantys/plone-heroku.git
heroku git:remote -a "${APP_NAME}"
git push heroku master
heroku open
heroku logs -t
```

See `heroku.cfg` and `buildout.cfg` for examples.

Configure
=====================================

You can configure the buildpack or deploy button with this envs:

```bash
UI_URL="https://launchpad.net/plone/5.0/5.0.4/+download/Plone-5.0.4-UnifiedInstaller.tgz"
UI_TARBALL="Plone-5.0.4-UnifiedInstaller.tgz"
UI_DIR="Plone-5.0.4-UnifiedInstaller"
BUILDOUT_CFG="heroku.cfg"
BUILDOUT_VERBOSITY="-v"
BOOTSTRAP_PY_URL="https://bootstrap.pypa.io/bootstrap-buildout.py"
CONFIGURE_ZOPECONF_URL="https://raw.githubusercontent.com/psychomantys/plone-heroku/master/configure_zopeconf.py"
ADMIN_NAME="admin"
ADMIN_PASSWD="admin"
```

Using the buildpack, you can set this like:

```bash
heroku config:add BUILDOUT_VERBOSITY=-vvvv
```

