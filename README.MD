Chowk
=====

Chowk acts as a interface between [RapidPro](http://rapidpro.io) and any number of [Kannel](http://kannel.org) servers that you have,
by passing messages to and fro in a format that both will understand.

Whom and how does Chowk help ?
----------------
If you have multiple Kannel servers and need to pass on each message originating from RapidPro
to the "right" kannel server based on the number series of the recipient (ie. the network operator),
chowk helps you.

Please note that Chowk only helps in case of 1-to-N connections of Rapidpro and Kannel servers and *not* vice versa.

Installation & usage
--------------------
see INSTALL section

Currently it:
-------------

* Takes a message from RapidPro and sends it to the Kannel server based on the starting series of the recipient's phone number.
* Forward a message from any Kannel server to the RapidPro instance.
* Send a confirmation report to RapidPro, of the message being successfully handed over to a Kannel server.
* Send a delivery reprot to RapidPro, when a Kannel server informs of message being delivered.
* Send a failure report to RapidPro, of any failures reported by any Kannel server.
* Use a single Celery powered task queue for processing messages

In future it will:
------------------
* Have better error messsages 
* E-mail based reporting 
* File based logging of exceptions, errors and warnings.
* Support SSL in connections with RapidPro and Kannel.
* Use Greenlet / eventlets to make things better, faster and easier (??)
* Authenticate requests from RapidPro and Kannel to ensure they are actually coming from where requests say they are coming.
* Priority based queue processing

What's in the name?
--------------------

Chowk is Hindi / Marathi for a traffic square where different routes meet and traffic is controlled, directed.
