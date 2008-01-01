# $Id$

load 'tasks/setup.rb'
ensure_in_path 'lib'
require 'webby'

task :default => 'spec:run'

PROJ.name = 'webby'
PROJ.summary = 'static website creation and management'
PROJ.authors = 'Tim Pease'
PROJ.email = 'tim.pease@gmail.com'
PROJ.url = 'http://webby.rubyforge.org/'
PROJ.description = paragraphs_of('README.txt', 3).join("\n\n")
PROJ.changes = paragraphs_of('History.txt', 0..1).join("\n\n")
PROJ.rubyforge_name = 'webby'
PROJ.rdoc_dir = 'doc/rdoc'
PROJ.rdoc_remote_dir = 'rdoc'
PROJ.version = Webby::VERSION


PROJ.exclude << '^examples/[^/]+/output'
PROJ.exclude << '^tasks/archive'
PROJ.exclude << '^tags$'

PROJ.rdoc_exclude << '^data'
PROJ.rdoc_exclude << '^examples'

PROJ.spec_opts << '--color'

depend_on 'directory_watcher', '1.1.0'
depend_on 'heel'
depend_on 'hpricot'
depend_on 'logging', '0.6.0'
depend_on 'rspec'

# EOF
