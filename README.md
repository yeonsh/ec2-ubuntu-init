# ec2-ubuntu-init

# /etc/environment

sudo echo "LC_ALL=en_US.UTF-8" | sudo tee --append /etc/environment
sudo echo "LANG=en_US.UTF-8" | sudo tee --append /etc/environment

# vim

git clone https://github.com/yeonsh/vim_settings.git
ln -s vim_settings/vimrc .vimrc
ln -s vim_settings/dot_vim .vim
rm -rf ./vim/bundle .vim/plugged .vim/plugin

sudo apt-get update
sudo apt-get install build-essential cmake
sudo apt-get install python-dev

vim -c "PlugInstall"

# elixir

wget https://packages.erlang-solutions.com/erlang-solutions_1.0_all.deb && sudo dpkg -i erlang-solutions_1.0_all.deb
sudo apt-get update
sudo apt-get install elixir

