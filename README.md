# prophet-bin
standalone python install, with fbprophet and its dependencies installed as compiled binaries (wheels), along with supporting system files for use on x86_64 Cent7

# Prerequisites
1. CentOS 7.4 x89_64 (previous versions of 7.x _*might*_ work as long as they're x86_64)
1. Decent amount of Linux devops expertise, because this comes with nearly no documentation and a lot of precursory knowledge is assumed...

# Setup
1. Add this to your .bashrc
```bash
# Python VirtualEnvWrapper
if [[ -e /usr/local/bin/virtualenvwrapper.sh ]]
then
   export WORKON_HOME=~/python3
   export VIRTUALENV_PYTHON=/usr/bin/python3
   source /usr/local/bin/virtualenvwrapper.sh
fi
```
2. extract mypy archive to your homedir
3. configure virtualenvwrapper to use the mypy python installation
4. make a symlink called /home/tommy and point it at your homedir (sorry, but that's how python was compiled in this case)
5. copy files from usr--bin.tar.xz to your /usr/bin directory (when in dobt, don't overwrite pre-existing files!)
6. copy files from usr--lib--python2.7--site-packages.tar.xz to /usr/lib/python2.7/site-packages (when in doubt, don't overwrite!)
