# Bootstrap Form

[![Build Status](https://travis-ci.org/dabit/bootstrap-form.png?branch=master)](https://travis-ci.org/dabit/bootstrap-form)

Form Helpers to make your form inputs [look like this](http://twitter.github.io/bootstrap/base-css.html#forms).

Helps you to create beautiful mocks really quickly.

Works with Bootstrap 2.3.0 and Rails 3.2+ (including Rails 4)

## Usage

Add the gem to your Gemfile

    gem 'bootstrap-form'

Bundle install

    bundle install

To make them look even better, I recommend you add this to your
application.rb

    ActionView::Base.field_error_proc = proc { |input, instance| input }

## Example

You write this:

    form_for @account do |f|
      f.bootstrap_text_field :name
    end


You get something like this:

    <div class="control-group">
      <label class="control-label" for="account_name">Name</label>
      <div class="controls">
        <input id="account_name" name="account_name" size="30" type="text">
      </div>
    </div>

Pretty straight forward.

## Custom Label

You can specify a custom label for the input by setting the label
option:

    form_for @account do |f|
      f.bootstrap_text_field :name, :label => 'A custom label'
    end

Then, you get something like this:

    <div class="control-group">
      <label class="control-label" for="account_name">A custom label</label>
      <div class="controls">
        <input id="account_name" name="account_name" size="30" type="text">
      </div>
    </div>

## Current Helpers List

* bootstrap_text_field
* bootstrap_password_field
* bootstrap_collection_select
* bootstrap_select
* bootstrap_file_field
* bootstrap_text_area
* bootstrap_email_field

## Error handling

All fields will automatically add the classes to show errors with Twitter
bootstrap styles.

## TODO

Coming soon:

* More form inputs
