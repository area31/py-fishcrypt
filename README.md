py-fishcrypt
============

FiSH/Mircryption clone for X-Chat in 100% Python

Requirements: PyCrypto, and Python 2.5+

Copyright 2011 Nam T. Nguyen ( http://www.vithon.org/forum/Thread/show/54 )
Released under the BSD license

Changelog:

   * 4.21
      + Fixed Empty Action /me

   * 4.20
      + Added support for Stealth mode >> no KeyExchange possible [/SET FISHSTEALTH True/False] 

   * 4.19
      + Added support for mIRC CBC KeyExchange, https://github.com/flakes/mirc_fish_10/ 

   * 4.18
      + Buffix Topic use key from channel not context

   * 4.17
      + CBC Default

   * 4.16
      + Bugfix Topic
      + config plaintextmarker in keyprotection
      + config parameter DEFAULTPROTECT and DEFAULTCBC

   * 4.15
      + Destroy object

   * 4.14
      + Stable

   * 4.13
      + new NickTrace
      + wildcard /KEY search
      + msg send to other target are marked with "Message Send"
      + Tab Completion for udpate command
      + using strxor from the pyCrypto packages if available
      + some performance enhancements
      + Pseudo Threading for Windows

   * 4.12
      + Beta Support

   * 4.11
      + BugFix /UPDATE

   * 4.10
      + BugFix /FISHSETUP

   * 4.09
      + BugFix again /FISHSETUP /UPDATE

   * 4.08
      + BugFix settings are not saved

   * 4.07
      + new Update function

   * 4.06
      + Small BugFixes

   * 4.05
      + BugFix Windows has no full xchatdir now using scriptpath for fish3.pickle

   * 4.04
      + BugFix notices

   * 4.03
      + BugFix /FISHSETUP

   * 4.02
      + noproxy oprions for /FISHSETUP

   * 4.01
      + BugFix pyBlowfish

   * 4.00
      + Windows Support with pyBlowfish.py and irccrypt now included

   * 3.31
      + BugFix unpack large messages

   * 3.30
      + Added chksum for irccrypt with __module_name__ tags http://pastebin.com/vTrWyBKv

   * 3.29
      + BugFix Update and Threaded Update

   * 3.28
      + /SET [fishcrypt]

   * 3.27
      + BugFix /ME+ in Query

   * 3.26
      + Updates over Proxy

   * 3.25
      + crypted /ME+ 

   * 3.24
      + BugFix topic 332

   * 3.23
      + BugFix notice send

   * 3.22
      + BugFix

   * 3.21
      + BugFix

   * 3.20
      + partly show incomplete messages

   * 3.19
      + /FISHUPDATE update switch

   * 3.18
      + AUTO CBC Mode only in querys

   * 3.17
      + Highlight Bugfix

   * 3.16
      + Highlight

   * 3.15
      + Bugfixes

   * 3.13
      + split lines if longer then 334 Chars 

   * 3.12
      + add PROTECTKEY to block dh1080 keyexchange on known Keys ( thx ^V^ )

   * 3.11
      + add Keystorage encryption

   * 3.10
      + Fix Path for Windows and provide download URL for pycrypto

   * 3.09
      + Bugfixes

   * 3.08:
      + some docu added

   * 3.07:
      + fixed notice in channel not send to user 

   * 3.06:
	   + support for /msg /msg+ /notice /notice+ (trubo)

   * 3.04:
	   + new lock design (by target) (trubo)

   * 3.01:
	   + change switches to be compatible with fish.secure.la/xchat/FiSH-XChat.txt (trubo)

	* 3.0:
	   + rewritten to class XChatCrypt (trubo)

   * 2.0:
      + Suport network mask in /key command
      + Alias key_exchange to keyx
      + Support plaintext marker '+p '
      + Support encrypted key store

   * 1.0:
      + Initial release

DESCRIPTION:
	rewritten by trubo/segfault for irc.prooops.eu #py-fishcrypt trubo00@gmail.com

	irccrypt module is copyright 2009 Bjorn Edstrom ( http://www.bjrn.se/ircsrp )
	with modification from Nam T. Nguyen and trubo
	
COMMANDS:
	/MSG+ send crypted msg regardless of /ENCRYPT setting
	/NOTICE+  : send crypted notice regardless of /ENCRYPT setting
	/ME+  : send crypted CTCP ACTION
	/SETKEY  : set a new key for a nick or channel
	/KEYX  : exchange pubkey for dialog
	/KEY  : show Keys
	/DELKEY  : delete Keys
	/CBCMODE  : enable/disable CBC Mode for this Key
	/ENCRYPT  : enable/disable encryption for this Key
	/PROTECTKEY  : enable/disable protection for keyx key exchange
	/DBPASS  : set/change the passphrase for the Key Storage
	/DBLOAD  : loads the Key Storage
	/PRNDECRYPT  : decrypts messages localy
	/PRNCRYPT  : encrypts messages localy
	/FISHUPDATE  : check online for new Version and update
	/SET [fishcrypt]  : show/set fishcrypt settings
