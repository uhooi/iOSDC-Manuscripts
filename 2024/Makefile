.PHONY: setup
setup:
	$(MAKE) install-ruby
	$(MAKE) install-gems

.PHONY: install-ruby
install-ruby:
	cat .ruby-version | xargs rbenv install --skip-existing

.PHONY: install-gems
install-gems:
	bundle config path vendor/bundle
	bundle install --without=documentation --jobs 4 --retry 3

.PHONY: update-gems
update-gems:
	bundle config path vendor/bundle
	bundle update --jobs 4 --retry 3
