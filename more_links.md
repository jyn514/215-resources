# Resources

Various useful resources from around the web.

## Getting help

- [Wikipedia](https://en.wikipedia.org)
- [Stack Overflow](https://stackexchange.com/)
- [IRC](https://webchat.freenode.net)
<sup>[(What is IRC?)](https://en.wikipedia.org/wiki/Internet_Relay_Chat)</sup>
- [Linux](https://www.tldp.org/)
- [Using `man` pages](https://askubuntu.com/questions/991946/how-can-i-get-help-on-terminal-commands)
on StackOverflow. I learned some things from this.

### More on man pages
- [Intro](https://ryanstutorials.net/linuxtutorial/manual.php)
- [Format](https://liw.fi/manpages/)
- [Linux](https://linux.die.net/man/)
- [Coreutils](https://www.gnu.org/manual/)

## Tools

### [Bash][bash man page]:

Bash is one of many [shells](https://en.wikipedia.org/wiki/Command-line_interface), which
take input and execute programs.
I've made a very [simple shell](https://github.com/jyn514/C-plus-plus/blob/master/interpreter/interpreter.cpp)
in C++ if you'd like to see an example.
See also the original [sh](https://en.wikipedia.org/wiki/Bourne_shell).

- [Guide](https://www.tldp.org/LDP/abs/html/)
- [Configuration files](http://wiki.bash-hackers.org/howto/conffile);
for bash, `~/.bashrc` and `~/.profile`
- [Bash vs sh](https://stackoverflow.com/questions/5725296/difference-between-sh-and-bash#5725402)
- [Scripting](https://en.wikibooks.org/wiki/Bash_Shell_Scripting)

### Shell built-ins
- `help`: Gives instructions for shell built-ins
- `quit` or `exit` or 
[`<Control>-d`](https://www.gnu.org/software/emacs/manual/html_node/emacs/User-Input.html#User-Input):
exit the current process
- `~`: `$HOME`, the directory you start in when you log in.
- `cd`: change directory. Defaults to `~`.
- `pwd`: 'print working directory'
- `echo`: Echo literal strings to the terminal
- [`printf`](https://en.wikipedia.org/wiki/Printf_format_string#Format_placeholder_specification):
Echo interpreted strings to the terminal
- `history`: Command history; uses `~/.bash_history`
Generally used with the 'symbolic' `-s` flag, which allows directories to be linked.
- `kill`: force a background process to stop
- `umask`: Set default [file permissions][file permissions]

### Commands on disk
- `man` or `info`: Gives instructions for everything else
- `cat`: 'catenate' a file
- `mkdir`: Make directory
- `ls`: list (contents of  directory). Defaults to `ls $(pwd)`.
- `rm`: Remove. Be careful with this command, it has no undo button.
- `rmdir`: Remove directory. You'll use `rm -r` (remove recursive) much more than this.
- `chmod`: 'change mode', change [file permissions][file permissions]
- `ps`: 'process', shows current processes
- `which`: find where a command is located on disk; see also `type` and `command`
- `less` or `more` or `pg`: 'pager', shows part of a file at a time then returns you to command line
- `ln`: Link (make two files refer to the same piece of memory).
- `touch`: Create an empty file
- `date`: Output the current time and date, in various formats.
- `cal`: Print a graphical calander to the terminal
- `calendar`: BSD version of `cal`, prints events for the next few days
- `zip`: Compress and decompress `.zip` files
- `tar`: Archive and extract `.tar` files
- `gzip`: compress and decompress files
- `bzip2`: compress and decompress files. More efficient but slower than `gzip`.
- `wget`: 'webget', download files without interaction
- `curl`: More modern `wget`
- `xdg-open`: Open files by their filetype, exactly as if clicked on in a GUI
- [`telnet`](https://en.wikipedia.org/wiki/Telnet): 'Teletype network',
access remote servers at the lowest application level
- `links` or `lynx` or `elinks`: terminal based web browsers
- `dhclient`: Negotiates an IP address from a router. For ethernet exclusively.
- `ip` or `ipconfig`: Various ip related config, information, and commands
- `cron` or `anacron` or `crond`: Executes background tasks at scheduled times. See also `crontab`.

#### Advanced commands
- [`ssh`](https://www.openssh.com/):
'Secure shell'; connects to a remote computer and executes programs.
This is the way you will usually log on to the lab computers, i.e.
`ssh <network username>@<ip address> -p <port>`.
See also options for [config files](https://www.ssh.com/ssh/config/)

- [`make`](https://www.gnu.org/software/make/manual/html_node/index.html#Top):
Automated build tool so you don't have to type as much.
See my [template](https://github.com/okeefe/215-resources/blob/master/template.makefile)
for a (fairly complicated) example,
or my [working makefile](https://github.com/jyn514/C-plus-plus/blob/master/makefile) for a simpler one.

- [`gcc`](https://gcc.gnu.org/onlinedocs/gcc-7.2.0/gcc/):
multi-language compiler. In this course we will be using `g++`,
but all of the gnu compilers are often used.

- [git](https://git-scm.com/book/en/v2):
[version control](https://git-scm.com/book/en/v2/Getting-Started-About-Version-Control)
so you can keep track of the changes you've made.
See also:
    - Git [subreddit](https://reddit.com/r/git)
    - Github [tutorials](https://help.github.com/)
    - Github [workshop](https://github.com/open-it-lab/git-workshop/blob/master/notes.sh)

- [GitHub][github]:
free online hosting for your git repos.
[This page](https://github.com/okeefe/215-resources)
is hosted there, as are various other resources.

- [`gpg`](https://gnupg.org): Encrypt and decrypt messages.
`gpg` was used by Snowden during the leaks of 2013
([Source](https://theintercept.com/2014/10/28/smuggling-snowden-secrets/))

- [`apt`](https://wiki.debian.org/Apt):
[package manager](https://en.wikipedia.org/wiki/Package_manager),
in some ways similar to an app store.
Most tools in this course are provided by the
[coreutils](https://www.gnu.org/software/coreutils/manual/html_node/index.html)
package, created by the [GNU project](https://www.gnu.org/software/software.html).
`g++` (and most other free compilers) use the [binutils](https://www.gnu.org/software/binutils/)
package, which contains tools necessary for compiling and debugging (assemblers, hexdumps, etc).

- [`screen`](http://aperiodic.net/screen/): Run multiple processes (in the foreground) at once

## [UNIX](https://www.opengroup.org/unix) <sup>[(What is UNIX?)][unix]</sup>

### Tutorials
Vaguely in order of how much I recommend them.

1. https://www.ee.surrey.ac.uk/Teaching/Unix/
2. https://heather.cs.ucdavis.edu/~matloff/unix.html
3. https://www.tutorialspoint.com/unix/

### History
- [Overview](https://www.cse.sc.edu/~pokeefe/tutorials/UnixHistory.html)
- [Wikipedia][unix] page
- [Development history](https://www.bell-labs.com/history/unix/)
- [Timeline](http://www.unix.org/what_is_unix/history_timeline.html)

#### Linux

- [Overview](https://www.youtube.com/watch?v=WVTWCPoUt8w) by 
[Linus Torvalds](https://en.wikipedia.org/wiki/Linus_Torvalds), creater of the Linux kernel
- [Wikipedia entry](https://en.wikipedia.org/wiki/History_of_Linux)
- [First mailing lists](https://groups.google.com/forum/#!msg/comp.os.minix/dlNtH7RRrGA/SwRavCzVE7gJ)
(not original site)
- [Kernel wars](https://web.archive.org/web/20121003060514/http://www.dina.dk/~abraham/Linus_vs_Tanenbaum.html)
- [GNU Project](https://en.wikipedia.org/wiki/GNU_Project)
- [Free software](https://en.wikipedia.org/wiki/History_of_free_and_open-source_software)
- [Stallman](https://en.wikipedia.org/wiki/Richard_Stallman); see also https://stallman.org

##### Installing Linux
- [Windows subsytem for Linux](https://msdn.microsoft.com/en-us/commandline/wsl/install-win10)
- [Dual-booting](https://www.howtogeek.com/187789/dual-booting-explained-how-you-can-have-multiple-operating-systems-on-your-computer/)

###### Distros <sup> [(What's a distro?)](https://en.wikipedia.org/wiki/Linux_distribution)</sup>

- [Debian](https://www.debian.org/intro/about)
- [Ubuntu](https://www.ubuntu.com/) is used in the Linux labs, based on debian
- [Fedora](https://getfedora.org/en/)
- [More info than you want](https://en.wikipedia.org/wiki/Comparison_of_Linux_distributions)

### Misc
- [Forums](https://www.unix.com/)
- [Unix FAQ](http://www.faqs.org/faqs/unix-faq/faq/part1/)
- [Unix Guru Universe](http://www.ugu.com/sui/ugu/show?help.beginners)
- [Lots more](http://www.catb.org/~esr/faqs/)

## Editors
I refuse to start an editor war. Find the editor wars on your own.

### For terminals

- [vim](https://vim.sourceforge.io/)
- [emacs](https://www.gnu.org/software/emacs/), which is graphical as well
- [nano](https://www.nano-editor.org/)
- [ed](https://www.gnu.org/fun/jokes/ed-msg.html)

### For Linux
- [kate](https://kate-editor.org/)
- [gedit](https://wiki.gnome.org/Apps/Gedit)

### For Windows
- [Notepad](https://en.wikipedia.org/wiki/Microsoft_Notepad)
- [Notepad++](https://notepad-plus-plus.org/)

### General purpose [IDE](https://en.wikipedia.org/wiki/Integrated_development_environments)s
- [Atom](https://atom.io/)
- [Brackets](http://brackets.io/)
- [Sublime text](https://www.sublimetext.com/)
- [Visual Studio Code](https://code.visualstudio.com/)


## [Languages](https://en.wikipedia.org/wiki/Programming_language)

### C++

- [Homepage](https://isocpp.org/)
- [Getting started](https://isocpp.org/get-started)
- [Tour](https://isocpp.org/tour)
- [Further resources](https://stackoverflow.com/questions/388242/the-definitive-c-book-guide-and-list)
- [Styleguide](http://www.stroustrup.com/bs_faq2.html)
- Draft of [official standard](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2014/n4296.pdf)
- Detailed [discussion](http://www.stroustrup.com/new_learning.pdf) (Article, PDF) of very basics

#### Tutorials
- https://www.cplusplus.com/doc/tutorial/
- https://www.learncpp.com/
- https://www.tutorialspoint.com/cplusplus/

#### Reference
- http://en.cppreference.com/w/cpp
([secure site](https://en.cppreference.com/w/cpp) looks ugly)
- https://www.cplusplus.com/doc/
- Wikimedia [ebook](https://en.wikibooks.org/wiki/C%2B%2B_Programming)


### Perl
- [Homepage](https://www.perl.org/) and [Intro](https://learn.perl.org/)
- [Wikipedia article](https://en.wikipedia.org/wiki/Perl)
- [Tutorial](https://users.cs.cf.ac.uk/Dave.Marshall/PERL/node1.html), HTML
- [Beginning Perl](https://learn.perl.org/books/beginning-perl/) (Book, HTML)
- Modern Perl (Book, [PDF](http://onyxneon.com/books/modern_perl/modern_perl_2016_a4.pdf),
[HTML](http://modernperlbooks.com/books/modern_perl_2016/))
- Various other tutorials: [1](https://www.tutorialspoint.com/perl/), 
[2](https://www.perl.com/pub/2000/10/begperl1.html),
[3](http://www.perltutorial.org/)

### Awk
- [GNU Manual](http://doc.cat-v.org/unix/v8/awktut.pdf)
- [1975 Manual](https://www.gnu.org/software/gawk/manual/gawk.html)

### Web
- [Handy infographic](https://i.redd.it/0nodknkfbxcz.jpg)
- [HTML reference](https://www.w3schools.com/html/default.asp )
- [Mozilla intro](https://developer.mozilla.org/en-US/docs/Learn)
- [XSS](https://www.google.com/about/appsecurity/learning/xss/)

## Algorithms
- [Urbana-Champaign](https://web.engr.illinois.edu/~jeffe/teaching/algorithms/),
various helpful resources
- [Princeton](https://algs4.cs.princeton.edu/home/)
- [Princeton, 2](https://www.cs.princeton.edu/~wayne/kleinberg-tardos/)
- [Approximation](https://www.cc.gatech.edu/fac/Vijay.Vazirani/book.pdf)
- [UCal](https://www.cse.iitd.ernet.in/~naveen/courses/CSL630/all.pdf) (with Quantum!)
- [Elementary algorithms](https://github.com/liuxinyu95/AlgoXY)
- MIT [Video lectures](https://ocw.mit.edu/courses/electrical-engineering-and-computer-science/6-046j-introduction-to-algorithms-sma-5503-fall-2005/video-lectures/)
- [Reference](https://www3.cs.stonybrook.edu/~algorith/) links

## Misc
- [Google guide](https://techdevguide.withgoogle.com), very career oriented
- [Course](http://mooc.fi/english.html) by U of Helsinki
- [Intro to Programming](https://pine.fm/LearnToProgram/) with Ruby
- [Intro to Programming](https://introcs.cs.princeton.edu/java/home/) with Java
- [Intro to Programming](https://introcs.cs.princeton.edu/python/home/) with Python
- LOTS of [links](http://freeprogrammingresources.com/)
- [Online compiler](https://repl.it/)
- [Reddit API](https:// praw.readthedocs.io)
- [Python](https://docs.python.org/3/)
- [Java](https://docs.oracle.com/javase/8/docs/api/)
- [Ruby](https://www.ruby-lang.org/en/documentation/)
- Misc open-source [docs](https://readthedocs.io)
- Obfuscate [email addresses](https://www.codeproject.com/Articles/8088/Avoiding-spam-bots) (to prevent spambots)

## File recovery
First, UNMOUNT THE DRIVE.

### Linux
- [debugfs](https://linux.die.net/man/8/debugfs)
- [ext3grep](https://packages.debian.org/stable/ext3grep)
- [ddrescue](https://packages.debian.org/stable/utils/gddrescue)
([GUI](https://packages.debian.org/stable/ddrescueview))
- with [Midnight Commander](https://www.datarecoverypros.com/recover-linux-midnightcommander.html)
- [extundelete](http://extundelete.sourceforge.net/)
([Guide](https://wiki.archlinux.org/index.php/file_recovery#Extundelete))
- [e2fsck](http://phpunixman.sourceforge.net/index.php/man/e2fsck/8)
- [ext4magic](http://ext4magic.sourceforge.net/ext4magic_en.html)

### Windows
- [Freeware](https://www.piriform.com/recuva), closed-source but works reliably
([direct link](https://download.piriform.com/rcsetup153.exe))

### Both
- [Foremost][foremost],
developed by the US Air Force Office of Special Investigations
- [Scalpel](https://github.com/sleuthkit/scalpel), based on [Foremost][foremost]
- [TestDisk](https://www.cgsecurity.org/wiki/TestDisk),
can recover unbootable partitions
- [PhotoRec](https://www.cgsecurity.org/wiki/PhotoRec), specializes in images

### More suggestions
- [Stack Overflow](https://unix.stackexchange.com/questions/80270/)
- [Arch Wiki](https://wiki.archlinux.org/index.php/file_recovery)
- Making [complete disk copies](https://wiki.archlinux.org/index.php/Disk_cloning)
from the Arch Wiki

## Neural Networks:
- [Courses by MIT](https://courses.csail.mit.edu/)
- [Tensorflow](https://www.tensorflow.org/get_started/), a Python framework for machine learning
- [Intro to core concepts](http://neuralnetworksanddeeplearning.com/)
- [More links](http://deeplearning.net)

## Challenge sites
- [Simple intro to challenge sites](http://codingbat.com)
- [Exercism](http://exercism.io): challenges of every level in every language
- [Project Euler](https://projecteuler.net), heavily math-based
- [Over the Wire](https://overthewire.org)
- [CodeWars](https://codewars.com)
- [Community pentests](https://vulnhub.com)
- [Python interactive challenges](https://github.com/donnemartin/interactive-coding-challenges/), heavy download
- [More links](https://softwareengineering.stackexchange.com/questions/756)

## Hosting
- [GitHub][github]
- [GitHub Pages](https://pages.github.com/)
- https://bitbucket.org/
- https://wordpress.com
- https://sourceforge.net
- [Digital Ocean](https://www.digitalocean.com/), hosts
[Docker containers](https://www.docker.com/what-docker). Costs money.

## More Resources
- [Free Programming Books](https://github.com/EbookFoundation/free-programming-books/blob/master/free-programming-books.md)
- [List of Lists of Resources](https://github.com/sindresorhus/awesome)

[bash man page]: https://www.gnu.org/software/bash/
[github]: https://github.com
[unix]: https://en.wikipedia.org/wiki/Unix
[file permissions]: https://www.linux.org/threads/file-permissions-chmod.4124/
[foremost]: http://foremost.sourceforge.net/
