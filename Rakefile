desc 'Inotify test'
task :inotify do
  require 'bundler'
  Bundler.require
  puts "inotify: running..."
  notifier = INotify::Notifier.new

  watch_path = "."

  puts "Watching at #{watch_path}"

  notifier.watch(watch_path, :modify, :create) do |event|
    puts "New event! Data changed in #{event.absolute_name}"
  end

  puts "Notifier up and running. Patchuuu!"
  notifier.run
end
