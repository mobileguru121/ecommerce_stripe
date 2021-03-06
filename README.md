# Ecommerce with Stripe

Project to test out integrating Stripe into Ruby on Rails with email sending and admin functionality.

## Demo

[https://commerce-stripe.herokuapp.com/](https://commerce-stripe.herokuapp.com)

## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes. See deployment for notes on how to deploy the project on a live system.

### Prerequisites

```
ruby 2.4.1
Rails 5.1.0
```

You will also need a [Stripe](https://stripe.com/) account.

### Installing

To get a development environment running:

```
git clone https://github.com/mobileguru121/ecommerce_stripe.git
cd ecommerce_stripe
bundle install
PUBLISHABLE_KEY=pk_test_your_Stripe_publishable_key SECRET_KEY=sk_test_your_Stripe_secret_key rails s
```

Visit [localhost:3000](http://localhost:3000/) in your browser.

## Deployment to Heroku

You will a [Heroku](https://www.heroku.com) account and these programs installed:

```
heroku-cli/5.9.4
git version 2.11.0
```

To deploy to Heroku:

```
heroku login
heroku create your-unique-app-name
heroku config:set PUBLISHABLE_KEY=pk_test_your_Stripe_publishable_key SECRET_KEY=sk_test_your_Stripe_secret_key
git push heroku master
heroku open
```

To create db on Heroku
```
heroku run rake db:create
heroku run rake db:migrate
heroku run rake db:seed
```

Heroku sendgrid
```
heroku addons:create sendgrid:starter
heroku config:get SENDGRID_USERNAME
appXYZ@heroku.com
heroku config:get SENDGRID_PASSWORD
password
Go [here]https://app.sendgrid.com/settings/api_keys
heroku config:set SENDGRID_API_KEY=xxxx_api_key_xxxx
```

To push updates to Heroku:

```
git push heroku master
```

Admin
```
user_name: admin@example.com
password: password
```

## Built With

* [Rails](http://rubyonrails.org/) - The web framework used
* [Stripe](https://rometools.github.io/rome/) - Payments
* [activeadmin](https://activeadmin.info/) - Administration framework

## Acknowledgments
