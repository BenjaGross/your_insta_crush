ENV["SINATRA_ENV"] ||= "development"

require_relative './config/environment'

# Type `rake -T` on your command line to see the available rake tasks.

namespace :db do
  task :migrate => :environment do
    ActiveRecord::Migrator.migrate('db/migrate')
  end

  task :rollback => :environment do
    ActiveRecord::Migrator.rollback('db/migrate')
  end

  task :drop => :environment do
    ActiveRecord::Migrator.migrate('db/migrate', 0)
  end
end


task :console do
  Pry.start
end