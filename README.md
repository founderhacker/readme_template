# Project Name Here
<project> does X for Y because Z.

## Installation
1. clone the repo
2. `cd <project> && bundle`
3. `rails db:setup && rails db:migrate`
4. `bundle exec figaro install`
5. get `config/application.yml` values from repo admin

## Development
```
bin/dev # uses foreman gem to boot server + frontend
```

## Testing (DELETE if n/a)
```
bundle exec rspec # run all tests inside spec/
bundle exec rspec spec/dir_name # run all tests inside given directory
```

## Deploying (DELETE if n/a)
install the [Heroku CLI](https://devcenter.heroku.com/articles/heroku-cli) and run `heroku login`. if repo admin has shared access to the server:

```
heroku git:remote -a heroku_app_name_here # you only need to do this once
git push heroku master # deploys master branch
git push heroku some_branch_name:master # deploys non-master branch
```

## Production management
to access the Rails console on the production server:
```
heroku run rails console
```
to add or update environment variables from your local `config/application.yml` file:
```
figaro heroku:set -e production
```
