Description
-----------

This script signals the health of a Drupal website by checking the following criteria:

* main database responds to queries
* slave database (if configured) responds to queries
* Memcached instances are available
* files directory is writeable
* temp directory is writeable

If at least one of these checks fails, the script returns a server error (code 500).


Installation
------------

Simply put the script into the root directory of your Drupal installation. Configure your load balancer to call it in its health check.


Authors
-------

This script is based on the status.php script from the Lullabot blog post ["Configuring Varnish for High-Availability with Multiple Web Servers"][1].

It has been adapted for [DrupalCONCEPT High Performance Drupal Hosting][2] by Jochen Lillich <jochen@freistil.it>.

[1]: http://www.lullabot.com/articles/varnish-multiple-web-servers-drupal
[2]: http://www.drupalconcept.com
