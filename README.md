<h1>PentBox</h1>

-----------------
PenTBox Tutorial
-----------------

https://www.kalilinux.in/2019/05/honeypot.html

<b>This repository is very old.  I didn't know much about Pentbox. I hop You Merge this Pull request to count My Pull Request .[No typo fix, REAL Update]</b>

<b> Pentbox is a safety kit containing various tools for streamlining PenTest conducting a job easily. It is programmed in Ruby and oriented to GNU / Linux, with support for Windows, MacOS and every systems where Ruby is installed.</b>

-----------------
How to Install
-----------------

git clone https://github.com/technicaldada/pentbox

cd pentbox

tar -zxvf pentbox.tar.gz

cd pentbox

./pentbox.rb

-----------------
PenTBox Changelog
-----------------

Version 1.8
-----------
New features:
- Command execution in gets (STDIN) implemented. (!command)
- Honeypot now shows attacker's IP and port (thx Shyish)
- Ip grabber direct targeting from email: yahoo,gmail,hotmail & sites like facebook gmail ...etc
- Included log options.
- Wordlist is bigger now.
- Included "back" option on menus.
New tools:
- Included new area, Web tools.
- Included new module MAC address geolocation (samy.pl).
- Included new module HTTP directory bruteforce.
- Included new module HTTP common files bruteforce.
- Included exploits for DoS
	[other/http] 3Com SuperStack Switch DoS
	[other/http] 3Com OfficeConnect Routers DoS (Content-Type)
	[windows/ftp] Windows 7 IIS7.5 FTPSVC UNAUTH'D DoS
	[windows/ftp] Solar FTP Server 2.1 DoS
	[windows/pptp] MS02-063 PPTP Malformed Control Data Kernel DoS
	[windows/smb] Windows Vista/7 SMB2.0 Negotiate Protocol Request DoS BSOD
- Included pb_update.rb to update PenTBox from the SVN repository.
Bugfixing:
- Fixed issue with SHODAN API.
- Deleted l33t speak and extra menu.
- Improved permissions checking, now it's done by euid, not username (thx r4mosg)

Version 1.4 & 1.5
-----------
- Code adapted to work with ruby1.9.x and jruby (more performance, native threads ...).
- Optimized TCP port scanner, and ping check before scan.
- Optimized hash_cracker.rb
- Renewed interface with colors (only unix-like) and improvements.

- Included RIPEMD-160 to Hash Password Cracker and Multi-Digest.
- Added native mode in SYN DoS that uses Raw Sockets.
- Added a new mode in the fuzzer -> HTTP headers client fuzzing.
- Added protected mode -> Only root can use DoS tools, excellent for installations in servers.
- Added a simple configuration in pentbox.rb for interface colors and protected mode.

- Unified syn_dos.rb and tcp_dos.rb in one, net_dos.rb
- Included pentbox-wlist.txt, that can be used with hash_cracker.rb
- New libraries bit-struct, net/dns.rb and racket.
- dns_search.rb included -> DNS and host gathering with NS, MX, SHODAN, A bruteforce and PTR IP range.

- tcp_dos_auto.rb excluded - To prevent from evil script-kiddies.
- fileencr.rb excluded - Crypto libraries was difficult to adapt, and the module
  was very slow. You can use openssl that is so much better and faster.
- sec_im.rb excluded - It wasn't used and not pentesting related.

Version 1.3.2
-------------
- FTP fuzzing improved and finished.
- Improved CLI.
- Improved files working.
- Now the Honeypot log have a file by default.
- Added a hping3-based mode to work in syn_dos.rb
- Added Dictionary attack and Dictionary-bruteforce
  hybrid attack in hash_cracker.rb
- Added SHA384 in digest.rb and hash_cracker.rb
- Now modules integration is with modules and classes,
  this improve the portability and the performance but
  the modules can't be executed independently.
- Fixed a couple of minor bugs.
- Minor improvements.

Version 1.3.1
-------------
- Added kB/s in TCP DoSer and TCP AutoDoSer.
- Fixed bug in packets counter in TCP DoSers.
- Updated readmes, now are more explicit and clear.
- Code revision (optimization, no bugs founded).

Version 1.3
-----------
- Added Crypt Ruby and RubyRc4 libraries.
- Added GOST, ARC4 and Rijndael (aka AES) 256 bits ciphers to Secure IM.
- Improvements in error exceptions and connection on Secure IM.
- fileencr.rb included -> Files encryptor and decryptor that uses Rijndael 256 bits, GOST and ARC4 ciphers.
- Included srand(time.now.to_i) function in programs that use random numbers.
- Added "Packets per second" in TCP DoSer and TCP AutoDoSer.
- Minor changes in titles of programs.

Version 1.2
-----------
- Added "beep() when intrusion" option in Honeypot.
- Added save log option in Honeypot.
- Fixed minor bugs.
- Updated GNU/GPLv3 License to 2010.
- Updated Readmes.
- Two new banners at startup.
- fuzzer.rb included -> Fuzzer to find vulnerabilities.
- hexa.rb deleted -> In Internet are a lot of converters.
- Now Secure password generator erases the variables from memory at the end.

Version 1.1
-----------
- sec_im included -> Secure IM Client, more info in the program.
- Improved Honeypot stability against DoS/DDoS Attacks.
- Improved general ortography and graphics.
- Added a lot of new code comments.
- Deleted Spanish code comments.
- Optimized tcp_dos.rb and tcp_dos_auto.rb
- Fixed small bugs in hash_cracker.rb
- hexa.rb included -> Hexadecimal converter.
- Re-Maked Menus.
- syn_dos.rb -> Modified Nmap installation and action command.

Version 1.0.1
-------------
- Modified code to be clearest and more simple in all archives.
- Added more error exceptions in Honeypot.
- Modified Default Web configuration in Honeypot.
- Fixed traduction problems in Readmes.
- Modified Windows .bat Loader.
- Base64 deleted from digest.rb and hash_cracker.rb
- Added this changelog.txt in the pack.

Version 1.0
-----------
- First version of the program.
