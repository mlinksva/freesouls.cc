require 'rubygems'
require_relative 'config/config.rb'
require_relative 'lib/freesouls_cc.rb'

desc "Fetch Flickr data"
task :sync do
  fcc = FreesoulsCC::Flickr.new(FLICKR_API_KEY, FLICKR_API_SECRET)
  fcc.sync(FLICKR_QUERIES, "photos")
end

desc "Generate templates"
task :gen do
  gen = FreesoulsCC::Jekyll.new("photos")
  gen.gen(FLICKR_QUERIES)
end
