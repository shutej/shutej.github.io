+++
date = "2015-01-17"
author = "Jeremy Shute"
title = "Putting MongoDB behind SSL using MMS"
+++

We use MongoDB for a variety of things at work.  However, there are not many
3rd party Mongo providers that offer SSL-protected connections at present.  We
need SSL for two reasons:

1. We have a bunch of services running on Heroku.  As a result, they need to
   access the database over the public internet.
2. Internal users want read-only access to query the data, or read-write access
   for prototyping or running tests.

The folks over at MongoDB offer MongoDB Management Service (MMS).  This is
actually a pretty excellent product if you're a startup: it has a paid backup
service, gives you the ability to easily manage replica sets, and is generally
very cost-competitive.

However, even if you are an Enterprise customer, at present MMS does not offer
a way to configure your database such that connections from the public internet
are SSL-protected.  Ouch.

Enter [my fork of Dvara](https://github.com/shutej/dvara).  Dvara is a
relatively new MongoDB proxy from the folks at Facebook.  Because Dvara is
written in Go, it took me only a few hours to add a few features.

1. The fork supports connecting over SSL if you pass `--key_file` and
   `--cert_file` command line flags.
2. The fork supports authenticating Dvara itself so that it is allowed to
   retrieve (only) the necessary replica information.

Here's a [Fabric](http://www.fabfile.org/) script that will let you set up
Dvara on your own AWS instances!  Read the `fabfile.py` carefully for usage
information.

{{% gist "shutej/0fe01b131d3a9868b232" %}}

I hope this will make it possible for others to keep their data flowing
securely!
