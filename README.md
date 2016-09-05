#TestBigData

This hadoop_common directory contains a snapshot of Wikipedia in a
.xml file, plus functioning codes that at this point can counts the
number of characters in each wikipedia entry, for the purpose of
comparing the lengths of the different entries.

Our plans is to adapt this code to do the same for the number of links
in each article, then ultimately extract all of the links and use them
as backbone of a program that will find the shortest route from one
entry to another, either chosen randomly or user supplied. Perhaps we
will ultimate create an interface with
http://thewikigame.com/speed-race with a DashSoft username so we can
perpetually finish first and draw at least a little attention to our
company.

****Install hadoop on Ubuntu:
http://www.bogotobogo.com/Hadoop/BigData_hadoop_Install_on_ubuntu_single_node_cluster.php

The biggest complication with the installation was with setting up
passkeys to localhost, believe it or not. ssh wanted me to use rsa
keys, while /etc/ssh/sshd_config only wanted to accept dsa keys. We
had to modify the PubkeyAcceptedKeyTypes to include ssh-rsa, after
which it functioned as needed.


****Start a java project in Intellij for Hadoop
http://blog.cloudera.com/blog/2014/06/how-to-create-an-intellij-idea-project-for-apache-hadoop/

****Link to codes that can scan wikipedia. Only one error in the code:
SimpleDateFormat ymdhms=new SimpleDateFormat("yyyy-MM-ddTHH:mm:ss"); /* ISO 8601 format */

requires single quotes around the T in the SDF string in order to compile:

SimpleDateFormat ymdhms=new SimpleDateFormat("yyyy-MM-dd'T'HH:mm:ss"); /* ISO 8601 format */

https://tpmoyer-gallery.appspot.com/hadoopWikipedia

**** Wikipedia dump can be found here:
https://meta.wikimedia.org/wiki/Data_dump_torrents#enwiki

I used this link:
http://burnbit.com/torrent/491258/enwiki_20160820_pages_articles_xml_bz2
