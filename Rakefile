# frozen_string_literal: true

#source "https://rubygems.org"
#require "bundler/gem_tasks"
require 'opal'
require 'opal-jquery'

task default: %i[]

namespace :opal do

  desc "Build our app to conway.js"
  task :build do
    builder = Opal::Builder.new
    builder.append_paths('app')
    builder.build('opal')
    builder.build('opal-jquery')
    builder.build("conway.rb")

    File.write "conway.js", builder.to_s
  end
end
