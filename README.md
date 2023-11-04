# shopy.dz
A web platform to enable merchants in Algeria to create ecommerce website for their busnesses and bring them online.
_NOTE:_ The platform is for the Algerian market
Shopy.dz
A platform similar to Shopify, BigCommerce, and YouCan for merchants to bring their business into the internet and manage it online.

# Features
The platform would allow merchants to do the following:

* Create their websites using some already made templates

* Edit the selected template of their websites by
  * Add more pages
  * Edit template pages
  * Edit styles of the website
  * Enable/Disable components
  * Change the layout of the pages
  * ... etc.

* Manage inventory of products (Add, Edit, Delete ...etc.)

* Manage orders from their customers
 
* Manage customers

* Allow customers to Register/Login/Logout
  * Manage customers shopping cards
  * Analytics about their customers, sales, products... etc.

* Manage shipping

* Integration with the shipping companies in Algeria through their APIs
  * Automatically update inventory after a product is shipped

* Other Features will be added as we go

# Development
## Requirements
* Ruby 3.2.2+
* Rails 7.1.1
* PostgresSQL 15+
* Redis 7.2+
* [Podman cli](https://podman-desktop.io/downloads) or [Podman Desktop](https://podman-desktop.io/downloads) or [docker](https://docs.docker.com/get-docker/)
## Setup
To setup the development environment:

### Install Ruby
We use [rvm](https://rvm.io) to manage the ruby versions
```bash
$ \curl -sSL https://get.rvm.io | bash -s stable
rvm install 3.2.2
bundle install
```

# Install Postgresql 15
Using `podman` or `docker`

```bash
podman pull docker.io/postgres:latest
# or
docker pull postgres:latest
```

# install Redis
Using `podman` or `docker`

```bash
podman pull docker.io/redis:latest
# or
docker pull redis:latest
```

# Run setup repository

```bash
# clone the repository with
git clone git@github.com:nafaabout/shopy.dz.git

cd shopy.dz


# Setup gems from Gemfile
bundle install -j 5 # run 5 bundle instances for quick install

rails db:create db:setup

# Run the application with
rails s

```
