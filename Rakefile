 task :default => 'install_plugin'
 
 task :install_plugin do
 
   sh "cp vimrc ~/.vimrc"
   sh "mkdir -p ~/.vim"
   sh "rm -rf ~/.vim/*"
   sh "cp -r * ~/.vim/" 
   
   puts "Install vim plugins "
   chdir "./bundle"
   sh "rm -rf *"
   File.open("../plugin.list") do |f|
     f.each_line do |repo|
       puts "#{repo}"
       sh "git clone #{repo}"
     end
   
   end
 end
