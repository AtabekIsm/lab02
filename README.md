armvo@LAPTOP-V7PSSN9N:~$ export GITHUB_USERNAME=AtabekIsm
armvo@LAPTOP-V7PSSN9N:~$ export GITHUB_EMAIL=atabekism@gmail.com
armvo@LAPTOP-V7PSSN9N:~$ export GITHUB_TOKEN=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
armvo@LAPTOP-V7PSSN9N:~$ lias edit=nano
lias: command not found
armvo@LAPTOP-V7PSSN9N:~$ alias edit=nano
armvo@LAPTOP-V7PSSN9N:~$ cd ${GITHUB_USERNAME}/workspace
-bash: cd: AtabekIsm/workspace: No such file or directory
armvo@LAPTOP-V7PSSN9N:~$ mkdir -p ${GITHUB_USERNAME}/workspace
armvo@LAPTOP-V7PSSN9N:~$ cd ${GITHUB_USERNAME}/workspace
armvo@LAPTOP-V7PSSN9N:~/AtabekIsm/workspace$ cd ${GITHUB_USERNAME}/workspace
-bash: cd: AtabekIsm/workspace: No such file or directory
armvo@LAPTOP-V7PSSN9N:~/AtabekIsm/workspace$ pwd
/home/armvo/AtabekIsm/workspace
armvo@LAPTOP-V7PSSN9N:~/AtabekIsm/workspace$ cd ..
armvo@LAPTOP-V7PSSN9N:~/AtabekIsm$ pwd
/home/armvo/AtabekIsm
armvo@LAPTOP-V7PSSN9N:~/AtabekIsm$ mkdir -p workspace/tasks/
armvo@LAPTOP-V7PSSN9N:~/AtabekIsm$ mkdir -p workspace/projects/
armvo@LAPTOP-V7PSSN9N:~/AtabekIsm$ mkdir -p workspace/reports/
armvo@LAPTOP-V7PSSN9N:~/AtabekIsm$ cd workspace
armvo@LAPTOP-V7PSSN9N:~/AtabekIsm/workspace$ wget https://nodejs.org/dist/v6.11.5/node-v6.11.5-linux-x64.tar.xz
--2025-05-04 10:40:31--  https://nodejs.org/dist/v6.11.5/node-v6.11.5-linux-x64.tar.xz
Resolving nodejs.org (nodejs.org)... 172.66.128.116, 104.20.3.6, 2606:4700:10::ac42:8074, ...
Connecting to nodejs.org (nodejs.org)|172.66.128.116|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 9356460 (8.9M) [application/x-xz]
Saving to: ‘node-v6.11.5-linux-x64.tar.xz’

node-v6.11.5-linux-x64.tar.xz 100%[=================================================>]   8.92M  3.89MB/s    in 2.3s

2025-05-04 10:40:34 (3.89 MB/s) - ‘node-v6.11.5-linux-x64.tar.xz’ saved [9356460/9356460]

armvo@LAPTOP-V7PSSN9N:~/AtabekIsm/workspace$ tar -xf node-v6.11.5-linux-x64.tar.xz
armvo@LAPTOP-V7PSSN9N:~/AtabekIsm/workspace$ rm -rf node-v6.11.5-linux-x64.tar.xz
armvo@LAPTOP-V7PSSN9N:~/AtabekIsm/workspace$ mv node-v6.11.5-linux-x64 node
armvo@LAPTOP-V7PSSN9N:~/AtabekIsm/workspace$ ls node/bin
node  npm
armvo@LAPTOP-V7PSSN9N:~/AtabekIsm/workspace$ echo ${PATH}
/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/games:/usr/local/games:/usr/lib/wsl/lib:/mnt/c/Program Files/WindowsApps/MicrosoftCorporationII.WindowsSubsystemForLinux_2.4.13.0_x64__8wekyb3d8bbwe:/mnt/c/WINDOWS/system32:/mnt/c/WINDOWS:/mnt/c/WINDOWS/System32/Wbem:/mnt/c/WINDOWS/System32/WindowsPowerShell/v1.0/:/mnt/c/WINDOWS/System32/OpenSSH/:/mnt/c/Program Files/Microsoft SQL Server/150/Tools/Binn/:/mnt/c/Program Files/Microsoft SQL Server/Client SDK/ODBC/170/Tools/Binn/:/mnt/c/Program Files/dotnet/:/mnt/c/Program Files/Git/cmd:/mnt/c/Users/armvo/AppData/Local/Microsoft/WindowsApps:/mnt/c/Users/armvo/.dotnet/tools:/mnt/c/Users/armvo/AppData/Local/GitHubDesktop/bin:/snap/bin
armvo@LAPTOP-V7PSSN9N:~/AtabekIsm/workspace$ export PATH=${PATH}:`pwd`/node/bin
armvo@LAPTOP-V7PSSN9N:~/AtabekIsm/workspace$ echo ${PATH}
/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/games:/usr/local/games:/usr/lib/wsl/lib:/mnt/c/Program Files/WindowsApps/MicrosoftCorporationII.WindowsSubsystemForLinux_2.4.13.0_x64__8wekyb3d8bbwe:/mnt/c/WINDOWS/system32:/mnt/c/WINDOWS:/mnt/c/WINDOWS/System32/Wbem:/mnt/c/WINDOWS/System32/WindowsPowerShell/v1.0/:/mnt/c/WINDOWS/System32/OpenSSH/:/mnt/c/Program Files/Microsoft SQL Server/150/Tools/Binn/:/mnt/c/Program Files/Microsoft SQL Server/Client SDK/ODBC/170/Tools/Binn/:/mnt/c/Program Files/dotnet/:/mnt/c/Program Files/Git/cmd:/mnt/c/Users/armvo/AppData/Local/Microsoft/WindowsApps:/mnt/c/Users/armvo/.dotnet/tools:/mnt/c/Users/armvo/AppData/Local/GitHubDesktop/bin:/snap/bin:/home/armvo/AtabekIsm/workspace/node/bin
armvo@LAPTOP-V7PSSN9N:~/AtabekIsm/workspace$ mkdir scripts
armvo@LAPTOP-V7PSSN9N:~/AtabekIsm/workspace$ cat > scripts/activate<<EOF
export PATH=\${PATH}:`pwd`/node/bin
EOF
armvo@LAPTOP-V7PSSN9N:~/AtabekIsm/workspace$ source scripts/activate
armvo@LAPTOP-V7PSSN9N:~/AtabekIsm/workspace$ gem install gist
Command 'gem' not found, but can be installed with:
sudo snap install ruby           # version 3.4.3, or
sudo apt  install ruby-rubygems  # version 3.4.20-1
See 'snap info ruby' for additional versions.
armvo@LAPTOP-V7PSSN9N:~/AtabekIsm/workspace$ sudo snap install ruby
[sudo] password for armvo:
error: This revision of snap "ruby" was published using classic confinement and thus may perform
       arbitrary system changes outside of the security sandbox that snaps are usually confined to,
       which may put your system at risk.

       If you understand and want to proceed repeat the command including --classic.
armvo@LAPTOP-V7PSSN9N:~/AtabekIsm/workspace$ sudo snap install ruby --classic
2025-05-04T10:43:20+03:00 INFO Waiting for automatic snapd restart...
ruby 3.4.3 from Ruby core team (rubylang✓) installed
armvo@LAPTOP-V7PSSN9N:~/AtabekIsm/workspace$ gem install gist
Fetching gist-6.0.0.gem
Successfully installed gist-6.0.0
1 gem installed

A new release of RubyGems is available: 3.6.7 → 3.6.8!
Run `gem update --system 3.6.8` to update your installation.

armvo@LAPTOP-V7PSSN9N:~/AtabekIsm/workspace$ export GITHUB_TOKEN=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
armvo@LAPTOP-V7PSSN9N:~/AtabekIsm/workspace$ (umask 0077 && echo ${GITHUB_TOKEN} > ~/.gist)
armvo@LAPTOP-V7PSSN9N:~/AtabekIsm/workspace$ source scripts/activate
armvo@LAPTOP-V7PSSN9N:~/AtabekIsm/workspace$ mkdir ~/.config
armvo@LAPTOP-V7PSSN9N:~/AtabekIsm/workspace$ cat > ~/.config/hub <<EOF
github.com:
- user: ${GITHUB_USERNAME}
  oauth_token: ${GITHUB_TOKEN}
  protocol: https
EOF
armvo@LAPTOP-V7PSSN9N:~/AtabekIsm/workspace$ git config --global hub.protocol https
armvo@LAPTOP-V7PSSN9N:~/AtabekIsm/workspace$ mkdir projects/lab02 && cd projects/lab02
armvo@LAPTOP-V7PSSN9N:~/AtabekIsm/workspace/projects/lab02$ git init
hint: Using 'master' as the name for the initial branch. This default branch name
hint: is subject to change. To configure the initial branch name to use in all
hint: of your new repositories, which will suppress this warning, call:
hint:
hint:   git config --global init.defaultBranch <name>
hint:
hint: Names commonly chosen instead of 'master' are 'main', 'trunk' and
hint: 'development'. The just-created branch can be renamed via this command:
hint:
hint:   git branch -m <name>
Initialized empty Git repository in /home/armvo/AtabekIsm/workspace/projects/lab02/.git/
armvo@LAPTOP-V7PSSN9N:~/AtabekIsm/workspace/projects/lab02$ git config --global user.name ${GITHUB_USERNAME}
armvo@LAPTOP-V7PSSN9N:~/AtabekIsm/workspace/projects/lab02$ git config --global user.email ${GITHUB_EMAIL}
armvo@LAPTOP-V7PSSN9N:~/AtabekIsm/workspace/projects/lab02$ git config -e --global
armvo@LAPTOP-V7PSSN9N:~/AtabekIsm/workspace/projects/lab02$ git remote add origin https://github.com/${GITHUB_USERNAME}/lab02.git
armvo@LAPTOP-V7PSSN9N:~/AtabekIsm/workspace/projects/lab02$ git pull origin master
fatal: couldn't find remote ref master
armvo@LAPTOP-V7PSSN9N:~/AtabekIsm/workspace/projects/lab02$ git pull origin main
remote: Enumerating objects: 9, done.
remote: Counting objects: 100% (9/9), done.
remote: Compressing objects: 100% (8/8), done.
remote: Total 9 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
Unpacking objects: 100% (9/9), 3.51 KiB | 327.00 KiB/s, done.
From https://github.com/AtabekIsm/lab02
 * branch            main       -> FETCH_HEAD
 * [new branch]      main       -> origin/main
armvo@LAPTOP-V7PSSN9N:~/AtabekIsm/workspace/projects/lab02$ ^C
armvo@LAPTOP-V7PSSN9N:~/AtabekIsm/workspace/projects/lab02$ touch README.md
armvo@LAPTOP-V7PSSN9N:~/AtabekIsm/workspace/projects/lab02$ git status
On branch master
nothing to commit, working tree clean
armvo@LAPTOP-V7PSSN9N:~/AtabekIsm/workspace/projects/lab02$ git add README.md
armvo@LAPTOP-V7PSSN9N:~/AtabekIsm/workspace/projects/lab02$ git commit -m"added README.md"
On branch master
nothing to commit, working tree clean
armvo@LAPTOP-V7PSSN9N:~/AtabekIsm/workspace/projects/lab02$ git push origin master
Username for 'https://github.com': AtabekIsm
Password for 'https://AtabekIsm@github.com':
remote: Support for password authentication was removed on August 13, 2021.
remote: Please see https://docs.github.com/get-started/getting-started-with-git/about-remote-repositories#cloning-with-https-urls for information on currently recommended modes of authentication.
fatal: Authentication failed for 'https://github.com/AtabekIsm/lab02.git/'
armvo@LAPTOP-V7PSSN9N:~/AtabekIsm/workspace/projects/lab02$ git push origin master
Username for 'https://github.com': AtabekIsm
Password for 'https://AtabekIsm@github.com':
remote: Support for password authentication was removed on August 13, 2021.
remote: Please see https://docs.github.com/get-started/getting-started-with-git/about-remote-repositories#cloning-with-https-urls for information on currently recommended modes of authentication.
fatal: Authentication failed for 'https://github.com/AtabekIsm/lab02.git/'
armvo@LAPTOP-V7PSSN9N:~/AtabekIsm/workspace/projects/lab02$ git push origin master
Username for 'https://github.com': AtabekIsm
Password for 'https://AtabekIsm@github.com':
remote: Support for password authentication was removed on August 13, 2021.
remote: Please see https://docs.github.com/get-started/getting-started-with-git/about-remote-repositories#cloning-with-https-urls for information on currently recommended modes of authentication.
fatal: Authentication failed for 'https://github.com/AtabekIsm/lab02.git/'
armvo@LAPTOP-V7PSSN9N:~/AtabekIsm/workspace/projects/lab02$ git push origin master
Username for 'https://github.com': AtabekIsm
Password for 'https://AtabekIsm@github.com':
remote: Support for password authentication was removed on August 13, 2021.
remote: Please see https://docs.github.com/get-started/getting-started-with-git/about-remote-repositories#cloning-with-https-urls for information on currently recommended modes of authentication.
fatal: Authentication failed for 'https://github.com/AtabekIsm/lab02.git/'
armvo@LAPTOP-V7PSSN9N:~/AtabekIsm/workspace/projects/lab02$ git push origin main
error: src refspec main does not match any
error: failed to push some refs to 'https://github.com/AtabekIsm/lab02.git'
armvo@LAPTOP-V7PSSN9N:~/AtabekIsm/workspace/projects/lab02$ git push origin master
Username for 'https://github.com':
Password for 'https://github.com':
remote: No anonymous write access.
fatal: Authentication failed for 'https://github.com/AtabekIsm/lab02.git/'
armvo@LAPTOP-V7PSSN9N:~/AtabekIsm/workspace/projects/lab02$ git push origin master
Username for 'https://github.com': AtabekIsm
Password for 'https://AtabekIsm@github.com':
remote: Invalid username or password.
fatal: Authentication failed for 'https://github.com/AtabekIsm/lab02.git/'
armvo@LAPTOP-V7PSSN9N:~/AtabekIsm/workspace/projects/lab02$ git push origin master
Username for 'https://github.com': AtabekIsm
Password for 'https://AtabekIsm@github.com':
remote: Support for password authentication was removed on August 13, 2021.
remote: Please see https://docs.github.com/get-started/getting-started-with-git/about-remote-repositories#cloning-with-https-urls for information on currently recommended modes of authentication.
fatal: Authentication failed for 'https://github.com/AtabekIsm/lab02.git/'
armvo@LAPTOP-V7PSSN9N:~/AtabekIsm/workspace/projects/lab02$ git push origin master

^C
armvo@LAPTOP-V7PSSN9N:~/AtabekIsm/workspace/projects/lab02$ git push origin master
^C
armvo@LAPTOP-V7PSSN9N:~/AtabekIsm/workspace/projects/lab02$ git push origin master
Username for 'https://github.com': AtabekIsm
Password for 'https://AtabekIsm@github.com':
remote: Support for password authentication was removed on August 13, 2021.
remote: Please see https://docs.github.com/get-started/getting-started-with-git/about-remote-repositories#cloning-with-https-urls for information on currently recommended modes of authentication.
fatal: Authentication failed for 'https://github.com/AtabekIsm/lab02.git/'
armvo@LAPTOP-V7PSSN9N:~/AtabekIsm/workspace/projects/lab02$ git push origin master
Username for 'https://github.com': AtabekIsm
Password for 'https://AtabekIsm@github.com':
remote: Support for password authentication was removed on August 13, 2021.
remote: Please see https://docs.github.com/get-started/getting-started-with-git/about-remote-repositories#cloning-with-https-urls for information on currently recommended modes of authentication.
fatal: Authentication failed for 'https://github.com/AtabekIsm/lab02.git/'
armvo@LAPTOP-V7PSSN9N:~/AtabekIsm/workspace/projects/lab02$ git push origin master
Username for 'https://github.com': AtabekIsm
Password for 'https://AtabekIsm@github.com':
remote: Invalid username or password.
fatal: Authentication failed for 'https://github.com/AtabekIsm/lab02.git/'
armvo@LAPTOP-V7PSSN9N:~/AtabekIsm/workspace/projects/lab02$ git push origin master
Username for 'https://github.com': AtabekIsm
Password for 'https://AtabekIsm@github.com':
Enumerating objects: 9, done.
Counting objects: 100% (9/9), done.
Delta compression using up to 12 threads
Compressing objects: 100% (8/8), done.
Writing objects: 100% (9/9), 3.53 KiB | 1.77 MiB/s, done.
Total 9 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), done.
remote:
remote: Create a pull request for 'master' on GitHub by visiting:
remote:      https://github.com/AtabekIsm/lab02/pull/new/master
remote:
To https://github.com/AtabekIsm/lab02.git
 * [new branch]      master -> master
armvo@LAPTOP-V7PSSN9N:~/AtabekIsm/workspace/projects/lab02$ git push origin master
Username for 'https://github.com': AtabekIsm
Password for 'https://AtabekIsm@github.com':
Everything up-to-date
armvo@LAPTOP-V7PSSN9N:~/AtabekIsm/workspace/projects/lab02$ git log
commit 1542f0f82ba411ff0c510060c0b37200f6b02271 (HEAD -> master, origin/master, origin/main)
Author: AtabekIsm <atabekism@gmail.com>
Date:   Fri May 2 18:46:37 2025 +0300

    Update README.md

commit 8f0bbe7b1d6fdc43b4fc90ecc69c7ae1d8fc061e
Author: AtabekIsm <atabekism@gmail.com>
Date:   Fri May 2 17:42:56 2025 +0300

    Create README.md

commit 563faa24e225199f8d141deb0208fc83aac79bdd
Author: AtabekIsm <atabekism@gmail.com>
Date:   Fri May 2 16:56:03 2025 +0300

    Initial commit
armvo@LAPTOP-V7PSSN9N:~/AtabekIsm/workspace/projects/lab02$ mkdir sources
armvo@LAPTOP-V7PSSN9N:~/AtabekIsm/workspace/projects/lab02$ mkdir include
armvo@LAPTOP-V7PSSN9N:~/AtabekIsm/workspace/projects/lab02$ mkdir examples
armvo@LAPTOP-V7PSSN9N:~/AtabekIsm/workspace/projects/lab02$ cat > sources/print.cpp <<EOF
#include <print.hpp>

void print(const std::string& text, std::ostream& out)
{
  out << text;
}

void print(const std::string& text, std::ofstream& out)
{
  out << text;
}
EOF
armvo@LAPTOP-V7PSSN9N:~/AtabekIsm/workspace/projects/lab02$ cat > include/print.hpp <<EOF
#include <fstream>
#include <iostream>
#include <string>

void print(const std::string& text, std::ofstream& out);
void print(const std::string& text, std::ostream& out = std::cout);
EOF
armvo@LAPTOP-V7PSSN9N:~/AtabekIsm/workspace/projects/lab02$ cat > examples/example1.cpp <<EOF
#include <print.hpp>

int main(int argc, char** argv)
{
  print("hello");
}
EOF
armvo@LAPTOP-V7PSSN9N:~/AtabekIsm/workspace/projects/lab02$ cat > examples/example2.cpp <<EOF
#include <print.hpp>

#include <fstream>

int main(int argc, char** argv)
{
  std::ofstream file("log.txt");
  print(std::string("hello"), file);
}
EOF
armvo@LAPTOP-V7PSSN9N:~/AtabekIsm/workspace/projects/lab02$ edit README.md
armvo@LAPTOP-V7PSSN9N:~/AtabekIsm/workspace/projects/lab02$ git status
On branch master
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        examples/
        include/
        sources/

nothing added to commit but untracked files present (use "git add" to track)
armvo@LAPTOP-V7PSSN9N:~/AtabekIsm/workspace/projects/lab02$ git add .
armvo@LAPTOP-V7PSSN9N:~/AtabekIsm/workspace/projects/lab02$ git commit -m"added sources"
[master 3324149] added sources
 4 files changed, 32 insertions(+)
 create mode 100644 examples/example1.cpp
 create mode 100644 examples/example2.cpp
 create mode 100644 include/print.hpp
 create mode 100644 sources/print.cpp
armvo@LAPTOP-V7PSSN9N:~/AtabekIsm/workspace/projects/lab02$ git push origin master
Username for 'https://github.com': AtabekIsm
Password for 'https://AtabekIsm@github.com':
Enumerating objects: 10, done.
Counting objects: 100% (10/10), done.
Delta compression using up to 12 threads
Compressing objects: 100% (7/7), done.
Writing objects: 100% (9/9), 927 bytes | 309.00 KiB/s, done.
Total 9 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/AtabekIsm/lab02.git
   1542f0f..3324149  master -> master
armvo@LAPTOP-V7PSSN9N:~/AtabekIsm/workspace/projects/lab02$




