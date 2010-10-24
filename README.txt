NoNonsenseForum © Copyright CC-BY-SA 3.0 Kroc Camen of Camen Design
===================================================================
A simple forum that focuses on discussion and simplicity


Requirements:
-------------
*	An up to date Apache installation, 2.2 or above
*	PHP 5.2.1 or above
*	A sub domain (like ‘forum.---.com’), virtual host or otherwise dedicated web-root for the forum.
	it will not run in a sub-folder


Install:
--------
1.	Copy this directory and all files to the web-root

2.	Create a folder named “users” on webroot

3.	Ensure the webroot and all sub-folders (especially “users”) have write permission for PHP,
	the code will save new threads directly to webroot

4.	Visit the site in your browser. if all is well, you should have an empty, but functional forum
	If you’re having problems you can ask for help on the forums: <forum.camendesign.com>


Creating Sub-Forums:
--------------------
If you would like to organise your forum into sub-forums for different topics just create a folder on webroot with the desired name (it can contain any letters except for “.”). Make sure the folder has write-permissions.


Stickying Threads:
------------------
If you would like a thread to always remain at the top of the threads list, also regardless of page number, create a file “sticky.txt” in the webroot or particular folder.

In your sticky.txt file add the filename of each thread you would like to sticky on separate lines, including the “.xml” file extension. For example:

the_rules.xml
f_a_q_.xml


Understanding Name Reservation:
-------------------------------
There is no login or registration of the traditional kind. In order to prevent someone’s desired name / nickname / alias / handle being reused by the wrong person, you enter your desired name and a password whenever you post. This name and password form a pair that have to match in order to use that name again in the future. Therefore you don’t have to log in beforehand, or pre-register before posting.

The single most important thing to bear in mind is that the name reservation system is not the same as authentication. Any person can enter any name they want and one person could just as easily use many names. It in no way ties one person to one browser session like a login does.

Whenever a name is reserved a text file is created in the users folder. The filename is a hash of the name and the file contains the hash of the password. Names are not case-sensitive, but passwords are.


Deleting a Thread:
------------------
The person who made a thread can delete their thread by clicking on the delete button in the first post of a thread. They then have to enter the name and password pair that was originally used to post to delete the thread.

Deleting individual posts is not supported at this early stage but will be added.


Adding Moderators:
------------------
Moderators can delete threads that were not originally made by them. to add moderators to your website, first have them post at least once in order to reserve the name. Then create a “mods.txt” file in webroot (per-folder mods are not supported at this moment, but will be) and populate it with the reserved names to allow moderator rights, one on each line. E.g.

Kroc
theraje
SpeedoJoe
