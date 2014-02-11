# WordPress-Url-Changer

A command line utility to change the name of a WordPress site.

## Status

![Incomplete](http://labs.cityindex.com/wp-content/uploads/2012/01/lbl-incomplete.png)![Unsupported](http://labs.cityindex.com/wp-content/uploads/2012/01/lbl-unsupported.png)

This project has been retired and is no longer being supported by City Index Ltd.

* if you should choose to fork it outside of City Index, please let us know so we can link to your project

## Scenario

1. You have an existing WordPress site running at mysite.com
1. You have a test version of that site running at test.mysite.com
1. You grab the files & a MySQL database dump of the mysite.com, 
copy them into the site root of the test.mysite.com site and restore the database dump over the test.mysite.com DB.
1. You run ```wordpress-url-changer --new_name test.mysite.com``` at the SSH terminal of test.mysite.com
    * This changes any Url references in the relevant config files (eg, wp-config.php)
    * This changes any Url reference in the relevant DB tables
1. You can now load http://test.mysite.com in your browser, and see a mirror of the live site in every respect except that the urls are different.

## Similar applications

1. https://github.com/interconnectit/Search-Replace-DB/blob/filestream/searchreplacedb2.php claims to handle search and replace of serialised PHP variables in the DB
1. ServerPress has this functionality as part of the scrubbing process it employs during site import
1. Creating this as a plugin for [wpcli](https://github.com/wp-cli/wp-cli) might provide a useful starting point eg. a way to extract the DB settings variables from the wp-config.php

## License

Copyright 2012 City Index Ltd.

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

  [http://www.apache.org/licenses/LICENSE-2.0](http://www.apache.org/licenses/LICENSE-2.0)

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
