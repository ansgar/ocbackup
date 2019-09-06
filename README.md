# ocbackup
## Simple shellscript to backup calendars and contacts from OwnCloud
This script provides a way to backup calendars and contacts from an OwnCloud-Installation.
It is meant to be used without user-interaction to be usable in a cronjob.
Consequently all information about the OwnCloud-Installation has to be stored in configuration files:

#### server
A file named server is expected to hold the information about the URL of the OwnCloud-DAV.
It is supposed to be stored in ~/.ocb and must contain one line with tabseparated values for
* protocol (http or https)
* host (the domainpart of the URL conceivably with subdomain)
* path (path to WebDAV in OwnCloud)
So an example for the file server should like this
    https ⇥ owncloud.example.com ⇥ remote.php/dav

#### calendar
A file named calendar is expected to hold the information about the calendars to be backed up.
It is also supposed to be stored in ~/.ocb and must contain one line for each single calendar with tabseparated values for
* username
* password
* calendarname
So an example for the file calendar should like this
    bob ⇥ supersecure123 ⇥ birthdays

#### contact
A file named contact is expected to hold the information about the addressbooks to be backed up.
As the other config files it is supposed to be stored in ~/.ocb and must contain one line for each single addressbook with tabseparated values for
* username
* password
* addressbookname
So an example for the file calendar should like this
    alice ⇥ i.wont.tell ⇥ private
