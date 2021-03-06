ionic-site
==========

Repo for the ionicframework.com site.  To preview local Ionic changes, follow the instructions at the [Ionic repo](https://github.com/driftyco/ionic#documentation).


gulp watch uses LiveReload. You may have to up your max file limit with the following command:

    ulimit -n 7000


## Local Build

    jekyll serve -w

    npm install

    sudo npm install -g gulp

    gulp watch

    http://localhost:4000/

## Deploy

Install [heroku-toolbelt](https://toolbelt.heroku.com/) or with homebrew

```bash
brew install heroku-toolbelt
```

Install [heroku-pipelines](https://devcenter.heroku.com/articles/pipelines)

```bash
heroku plugins:install heroku-pipelines
```

Then log into heroku

```bash
heroku login
# enter your email and password when promted
```

Then add the heroku remotes

```bash
git remote add production https://git.heroku.com/ionic-site.git
```

```bash
git remote add staging git@heroku.com:ionic-site-staging.git
```


- Make your changes
- Run `gulp`
- `git push origin master`
- View the staging server at [http://ionic-site-staging.herokuapp.com/](http://ionic-site-staging.herokuapp.com/)
- Promote the staging server to production
- `heroku pipelines:promote -r staging`
- Watch the build server at [https://circleci.com/gh/driftyco/ionic-site](https://circleci.com/gh/driftyco/ionic-site)

## Community

* Follow [@ionicframework on Twitter](https://twitter.com/ionicframework).
* Subscribe to the [Ionic Newsletter](http://ionicframework.com/subscribe/).
* Have a question that's not a feature request or bug report? [Discuss on the Ionic Forum](http://forum.ionicframework.com/).
* Read our [Blog](http://ionicframework.com/blog/).
* Have a feature request or find a bug? [Submit an issue](https://github.com/driftyco/ionic/issues).


## Authors

**Max Lynch**

+ <https://twitter.com/maxlynch>
+ <https://github.com/mlynch>

**Ben Sperry**

+ <https://twitter.com/benjsperry>
+ <https://github.com/bensperry>

**Adam Bradley**

+ <https://twitter.com/adamdbradley>
+ <https://github.com/adamdbradley>
