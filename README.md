Heroku on Plone Button
=====================================

Deploy Plone 5 with Plone with some modules.


<a href="https://heroku.com/deploy?template=https://github.com/psychomantys/plone-heroku" rel="some text">![Foo](https://www.herokucdn.com/deploy/button.png)</a>


This will deploy Plone with the following default login credentials(by default):

username: admin
password: admin

Buildpack
=====================================

```
heroku create --buildpack https://github.com/psychomantys/plone-heroku.git
heroku git:remote -a "${APP_NAME}"
git push heroku master
heroku open
heroku logs -t
```

