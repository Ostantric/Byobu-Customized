# Customized Byobu

For more information about this package, please see:
 * http://byobu.org

If Byobu is not packaged for your Linux or UNIX OS, or if you do not have
administrative privileges in order to install Byobu, you may be able to
install locally, using the following instructions...
## Installation
```bash
git clone https://github.com/Ostantric/Byobu-Customized.git byobu-src 
cd byobu-src
./debian/rules autoconf
cd byobu-src
./configure --prefix="$HOME/byobu"
```
### OPTIONAL:

 Use python from your environment, rather than from your distro
```bash
      echo "export BYOBU_PYTHON='/usr/bin/env python'" >> $HOME/.bashrc
```
### Build:
```bash
make
make install
```
### Update your PATH and BYOBU_PREFIX environment variables
```bash
echo "export PATH=$HOME/byobu/bin:$PATH" >> $HOME/.bashrc
. $HOME/.bashrc
```
### Run
```bash
      byobu
```
### Byobu as default
Add this in .bashrc
```bash
_byobu_sourced=1 . /home/murat/byobu/bin/byobu-launch 2>/dev/null || true
```
### Clear Byobu config directory before start using it
```
rm -rf ~/.byobu
```
