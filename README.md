![Logo WordCamp] (http://central.wordcamp.org/wp-content/themes/wordcamp-central-2012/images/wordcamp-central-logo.png)

WordCamp, The Netherlands
=========================

10-11 May 2014  
[Twitter hashtag #wcnl]  
Go to [WordCamp Central] website.

This short document contains all the sources u need to get started with Vagrant. Vagrant makes virtualization on the desktop easy, affordable and provides for a cleaner WordPress development experience. Make your development setup match production as close as possible and shareable. DTAP is nice for development but can become a nightmare to maintain and expensive. Combine Vagrant with one of it's Cloud providers like [DigitalOcean] and you create a affordable on-demand DTAP solution.

Vagrant
-------

Vagrant is a tool for building and distributing virtual environments. Together with a large array of virtualization providers like [Virtualbox] it caters for a complete development workflow. Vagrant as a project was founded by Mitchel Hashimoto and is currently supported by his company [HashiCorp].

Go to the project website of [Vagrant] it contains a lot of useful information and documentation though not overwhelming.

Project page of [Vagrant on Github] for those who want to study or hack on the source code.

Install Virtualbox and Vagrant
------------------------------

The 'Varying Vagrant Vagrants' project on Github has a [VVV get started] section, which explains all in detail and is up-to-date. Remember to download the 1.5.4 version of Vagrant because the newer 1.6 version has issues.

First install Virtualbox on your workstation, follow the instructions on the [download wiki page]. Second go to the [Vagrant download page] and follow the instructions. Should not be to difficult.

The [VVV get started] section also wants you to install some Vagrant plug-ins. Go ahead, you definitely want to <code>git clone</code> this project use it, adept it or study it.

If you have a need for other base boxes and you don't want to build them from scratch yourselves, go have a look at [Vagrantbox]. But be careful with unknown boxes from unknown sources, those from puppetlabs should be fine!

Vagrant and WordPress
---------------------

Now go to the Varying-Vagrant-Vagrants ([VVV]) Github page. It's a very active project which provides you with a Vagrantfile and a shell provisioning file to kick-start a complete WordPress development environment. The image used is Ubuntu 14.04 LTS Trusty Tahr (64 bit) and they build up the server using Nginx with PHP-FPM. After cloning the Git repo you also get a set of configuration files which are used during the 'Vagrant init' to set-up all services.

After a <code> $ vagrant up</code> you should be able to access [http://vvv.dev](http://vvv.dev/ "default dashboard page") if not edit your hosts file. I had to add a line <code>192.168.50.4    vvv.dev local.wordpress.dev local.wordpress-trunk.dev src.wordpress-develop.dev build.wordpress-develop.dev</code> to make it work.


Build Vagrant base boxes
------------------------

The next step is to build your own base boxes and share them with coworkers, clients etc. Building complete and usable base boxes takes time and (Ops) skills. Building new boxes which have to run on different providers could be a time consuming challange. Lucky us that projects like  [Veewee] and [Packer] came to town. [Packer] is a tool, from [HashiCorp], that lets you build Virtual Machine Images for different providers from just one json file. One word, awesome!

Project page of [Packer on Github] for those who want to study or hack on the source code.


Vagrant and Docker containers
-----------------------------

There is a nice [blog post] explaining the usefulness of the combination of Vagrant and [Docker]. It's where I got the quote "Docker does to Linux what git has done to source control." It has several other blog post on Docker. Container virtualization is a subject that will affect WordPress hosting for the years to come. Keep in mind that the project has not yet delivered it's first stable release, this is technology preview.

More Vagrant friends
---------------------

### PuPHPet
Control Vagrant & Puppet from a web GUI,really slick.
http://puPHPet.com

### Vagrant Cloud
Share, distribute and discover base boxes.
https://vagrantcloud.com/

### The Book (Dead trees and ebook)
Title:Vagrant: Up and Running  
By: Mitchell Hashimoto  
Publisher:O'Reilly Media Formats:  
Print  Ebook  Safari Books Online  
Print: June 2013  
Ebook: May 2013  
Pages: 158  
Print ISBN:978-1-4493-3583-0 | ISBN 10:1-4493-3583-7  
Ebook ISBN:978-1-4493-3582-3 | ISBN 10:1-4493-3582-9  



[Twitter hashtag #wcnl]: http://twitter.whotalking.com/topic/%23wcnl "Twitter hashtag #wcnl"
[WordCamp Central]: http://central.wordcamp.org/ "WordCamp Central website"
[HashiCorp]: http://www.hashicorp.com/ "Mitchell Hashimoto founder of HashiCorp"
[Vagrant]: http://vagrantup.com/ "Project website of Vagrant"
[Vagrant on Github]: https://github.com/mitchellh/vagrant "Github project page of Vagrant"
[Virtualbox]: https://www.virtualbox.org "Oracle Virtualbox webpage"
[DigitalOcean]: https://www.digitalocean.com "Website of Cloud provider Digital Ocean"
[download wiki page]: https://www.virtualbox.org/wiki/Downloads "Download Wiki page with Virtualbox binaries for Linux, Mac or Windows"
[VVV get started]: https://github.com/Varying-Vagrant-Vagrants/VVV#getting-started "Varying-Vagrant-Vagrants(VVV) getting-started webpage"
[Vagrant download page]: http://www.vagrantup.com/downloads.html "Vagrant download page with binaries for Linux, Mac and Windows"
[Vagrantbox]: http://www.vagrantbox.es/ "Vagrantbox website"
[VVV]: https://github.com/Varying-Vagrant-Vagrants/VVV "Varying-Vagrant-Vagrants(VVV) Github page"
[Veewee]: https://github.com/jedi4ever/veewee "Veewee Github project page"
[Packer]: http://www.packer.io/ "Packer website"
[Packer on Github]: https://github.com/mitchellh/packer "Packer Github project page"
[Docker]: https://www.docker.io/ "Docker website"
[blog post]: http://www.centurylinklabs.com/docker-vs-vagrant-cloud/ "docker vs vagrant cloud blog post"
