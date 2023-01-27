# Project


**FinanceTracker** is a comprehensive and user-friendly platform that allows users to track the US stock market and individual stocks, create and manage portfolios, and connect with other investors. With its powerful features and intuitive interface, FinanceTracker is the perfect tool for anyone looking to stay on top of their investments.

One of the key features of FinanceTracker is its real-time market data, which allows users to track the performance of individual stocks and the overall market. This feature makes it easy for users to stay informed about the latest market trends and make informed investment decisions.

Another great feature of FinanceTracker is the ability to create and manage portfolios. Users can add stocks to their portfolio and track their performance over time. Additionally, users can also see public portfolios of other users and get insights on how they are managing their investments.

FinanceTracker also offers a messaging functionality that allows users to connect with other investors and share tips, insights, and strategies. This feature makes it easy to build a community of like-minded investors and learn from one another.

Overall, FinanceTracker is a powerful and user-friendly platform that makes it easy to stay on top of your investments and connect with other investors. Whether you're a seasoned pro or a beginner, FinanceTracker has everything you need to manage your portfolio and make informed investment decisions.

## Install

### Clone the repository

```shell
git clone git@github.com:thepavankoushik/FinanceTracker.git
cd FinanceTracker
```

### Check your Ruby version

```shell
ruby -v
```

The ouput should start with something like `ruby 2.5.1`

If not, install the right ruby version using [rbenv](https://github.com/rbenv/rbenv) (it could take a while):

```shell
rbenv install 2.5.1
```

### Install dependencies

Using [Bundler](https://github.com/bundler/bundler) and [Yarn](https://github.com/yarnpkg/yarn):

```shell
bundle && yarn
```


### Initialize the database

```shell
rails db:create db:migrate db:seed
```

### Add heroku remotes

Using [Heroku CLI](https://devcenter.heroku.com/articles/heroku-cli):

```shell
heroku git:remote -a project
heroku git:remote --remote heroku-staging -a project-staging
```

## Serve

```shell
rails s
```

## Deploy

### With Heroku pipeline (recommended)

Push to Heroku staging remote:

```shell
git push heroku-staging
```

Go to the Heroku Dashboard and [promote the app to production](https://devcenter.heroku.com/articles/pipelines) or use Heroku CLI:

```shell
heroku pipelines:promote -a project-staging
```

### Directly to production (not recommended)

Push to Heroku production remote:

```shell
git push heroku
```
