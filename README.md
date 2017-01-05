Requirements
============

* Ruby 2.0 or greater (Using rvm for multiple Ruby management)
* Vagrant 1.8.1
* Bundler

```
gem install bundle
```

Build
=====

* Install dependencies

```
bundle install
```

* Create test machines

```
bundle exec kitchen create
```

* Apply playbook to machines(rerun if failed)

```
bundle exec kitchen converge
```

* Verify

```
bundle exec kitchen verify
```

* Destroy test machines

```
bundle exec kitchen destroy
```