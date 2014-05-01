# This file manages Puppet module dependencies.
#
# It works a lot like Bundler. We provide some core modules by
# default. This ensures at least the ability to construct a basic
# environment.

# Shortcut for a module from GitHub's boxen organization
def github(name, *args)
  options ||= if args.last.is_a? Hash
    args.last
  else
    {}
  end

  if path = options.delete(:path)
    mod name, :path => path
  else
    version = args.first
    options[:repo] ||= "boxen/puppet-#{name}"
    mod name, version, :github_tarball => options[:repo]
  end
end

# Shortcut for a module under development
def dev(name, *args)
  mod name, :path => "#{ENV['HOME']}/src/boxen/puppet-#{name}"
end

# Includes many of our custom types and providers, as well as global
# config. Required.

github "boxen",      "3.3.4"

# Core modules for a basic development environment. You can replace
# some/most of these if you want, but it's not recommended.

github "dnsmasq",      "1.0.1"
github "foreman",      "1.0.0"
github "gcc",          "2.0.1"
github "git",          "1.3.7"
github "go",           "2.0.1"
github "homebrew",     "1.6.0"
github "inifile",      "1.0.1", :repo => "puppetlabs/puppetlabs-inifile"
github "openssl",      "1.0.0"
github "phantomjs",    "2.1.0"
github "pkgconfig",    "1.0.0"
github "repository",   "2.3.0"
github "ruby",         "6.7.2"
github "stdlib",       "4.1.0", :repo => "puppetlabs/puppetlabs-stdlib"
github "sudo",         "1.0.0"
github "xquartz",      "1.1.1"
github "sysctl",       "1.0.0"

# Optional/custom modules. There are tons available at
# https://github.com/boxen.
github "osx",          "2.2.2"
github "python",       "1.3.0"
github "postgresql",   "3.0.1"
github "wget",         "1.0.1"
github "heroku",       "2.1.1"
github "flux",         "1.0.0"
github "ctags",        "1.0.0"
github "vim",          "1.0.5"
github "zsh",          "1.0.0"
github "oh_my_zsh",    "1.0.0", :repo => "blacktorn/puppet-oh_my_zsh"
github "chrome",       "1.1.2"
github "firefox",      "1.1.8"
github "iterm2",       "1.0.7"
github "alfred",       "1.1.7"
github "skitch",       "1.0.2"
github "sourcetree",   "1.0.0"
github "dropbox",      "1.2.0"
github "spotify",      "1.0.1"
github "virtualbox",   "1.0.10"
github "vagrant",      "3.0.4"
github "pathfinder",   "1.0.0", :repo => "blacktorn/puppet-pathfinder"
github "contexts",     "1.0.0", :repo => "blacktorn/puppet-contexts"
github "kaleidoscope", "1.0.4", :repo => "ngs/puppet-kaleidoscope"
github "intellij",     "1.4.0"
github "pgadmin3",     "1.0.0"
