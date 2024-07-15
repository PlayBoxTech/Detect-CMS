Detect-CMS
==========

PHP Library for detecting CMS

Install
-------

```bash
composer require playboxtech/detect-cms:dev-master
```
Based On:
-----------
    This is based on https://github.com/Krisseck/Detect-CMS as the author has stopped updating his, decided to pick up where he left off. 

Updated:
---------
    Updated the [PHP Simple HTML DOM Parser](https://sourceforge.net/projects/simplehtmldom/) from version 0.5 to 1.91 as it was having issues with newer versions of PHP.
    Added detection for GravCMS

TO DO:
------
    Further update detection to use new built in PHP functions so no longer need to depend on external library. 
    Detect additional types of CMS

How to use:
-----------

    include(__DIR__ . "/vendor/autoload.php");
    $domain = "http://google.com";
    $cms = new \DetectCMS\DetectCMS($domain);
    if($cms->getResult()) {
        echo "Detected CMS: ".$cms->getResult();
    } else {
        echo "CMS couldn't be detected";
    } 
