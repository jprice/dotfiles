```
##################################################
#    .___      __    _____.__.__                 #
#  __| _/_____/  |__/ ____\__|  |   ____   ______#
# / __ |/  _ \   __\   __\|  |  | _/ __ \ /  ___/#
#/ /_/ (  <_> )  |  |  |  |  |  |_\  ___/ \___ \ #
#\____ |\____/|__|  |__|  |__|____/\___  >____  >#
#     \/                               \/     \/ #
#                                                #
# about: custom . files                          #
# author: Josh Price                             #
#                                                #
##################################################
```

Dotfiles 
========
Based off [Dotphiles][1] see that repo for more info. I soon plan to switch to using Ansible to manage them. Maybe.

Installation
------------
Run dotsync `./.dotfiles/dotsync/bin/dotsync -L`

Configuration
-------------

See the documentation for [dotsync][2] for more information.

Backups
-------------
Any existing ~/.dotfiles will be backed up into `~/.backup/dotfiles/` if found


Oh-My-ZSH Theme Fix
-------------
This is only required if you use the trapd00r theme. Otherwise skip.

The them I use requires some extra steps in order to work. Just follow the following:


```
cd ~/bin # assume that your ~/bin exists and is in your $PATH
wget https://raw.githubusercontent.com/trapd00r/utils/master/zsh_path
chmod +x zsh_path

cd /tmp
wget http://search.cpan.org/CPAN/authors/id/W/WO/WOLDRICH/Term-ExtendedColor-0.224.tar.gz
tar xvzf Term-ExtendedColor*.tar.gz
cd Term-ExtendedColor*
perl Makefile.PL  # assuming you have perl-Makefile-Parser installed on your box
make
sudo make install
```



Credits
-------------

*[Conky](https://github.com/alexbel/conky)
*If I "stole" something from you and left you out please open an issue.

Contribute
------------
Feel free to fork and send Pull Requests.

License
-------

Copyright (c) 2015
Permission is hereby granted, free of charge, to any person obtaining
a copy of this software and associated documentation files (the
"Software"), to deal in the Software without restriction, including
without limitation the rights to use, copy, modify, merge, publish,
distribute, sublicense, and/or sell copies of the Software, and to
permit persons to whom the Software is furnished to do so, subject to
the following conditions:

The above copyright notice and this permission notice shall be
included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF
MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND
NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE
LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION
OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION
WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

[1]: https://github.com/dotphiles/dotphiles
[2]: https://github.com/dotphiles/dotsync
