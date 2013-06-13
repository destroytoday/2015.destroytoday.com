require 'rubygems'
require 'bundler'
require 'fileutils'
Bundler.require :default

task :zip do
  theme = File.join(File.dirname(__FILE__), 'theme.zip')

  FileUtils.rm(theme)

  Zip::ZipFile.open(theme, Zip::ZipFile::CREATE) do |zip|
    Dir.glob("**/*.{html,css,png,gif,jpg}").each do |path|
      zip.add(path, File.join(File.dirname(__FILE__), path))
    end
  end
end
