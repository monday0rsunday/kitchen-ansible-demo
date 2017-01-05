Requirements
============

* Ruby 2.0 or greater (Using rvm for multiple Ruby management)

```
gpg --keyserver hkp://keys.gnupg.net --recv-keys 409B6B1796C275462A1703113804BB82D39DC0E3
curl -sSL https://get.rvm.io | bash -s stable
source ~/.profile
rvm install 2.0
rvm use 2.0
```

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
Issues
======
There is problem with test-kitchen scp, see [test-kitchen issues 1035](https://github.com/test-kitchen/test-kitchen/issues/1035#issuecomment-222243544)(async, I guested). I drop test-kitchen to 1.8.0
