require "rubygems"
require "rake"

home_dir = "#{ENV['HOME']}/.vimrc"

desc "Deploy to codeography.com"
task :install do
  puts "Copying jekyll.vim to #{ENV['HOME']}/.vim"
  FileUtils.copy(File.dirname(__FILE__) + "/plugin/jekyll.vim", ENV['HOME'] + "/.vim/plugin")
  FileUtils.copy(File.dirname(__FILE__) + "/doc/jekyll.txt", ENV['HOME'] + "/.vim/doc")
  puts "Yay."
end

desc "Append key mappings"
task :append_mappings do
  open(home_dir, 'a') { |f|
    f << "\n"
    f << "\" jekyll.vim key mappings\n"
    f << "map <Leader>jn  :JekyllPost<CR>\n"
    f << "map <Leader>jl  :JekyllList<CR>\n"
    f << "map <Leader>jc  :JekyllCommit<CR>\n"
    f << "map <Leader>jp  :JekyllPublish<CR>\n"
  }
end
