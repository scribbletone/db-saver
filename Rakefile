require "pgbackups-archive"

class RunPgbackupsArchive
  def call
    Heroku::Client::PgbackupsArchive.perform
  end
end

namespace :pgbackups do

  desc "Perform a pgbackups backup then archive to S3."
  task :archive do
    RunPgbackupsArchive.new.call
  end

end
