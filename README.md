# mediawiki-pages-ResourceDirectory

Semantic structure, forms and templates for extendable resource annotation and browsing.

# Requirements
* Extension:SemanticMediaWiki
* Extension:PageForms
* Extension:Arrays
* Extension:PageExchange or Extension:PagePort

# Setup

## via PagePort
* Download the repository
* Run
```php
php extensions/PagePort/maintenance/importPages.php --source ~/mediawiki-pages-ResourceDirectory
```

## via PageExchange
* Add the following line to your LocalSettings.php:
```php
$wgPageExchangePackageFiles[] = 'https://raw.githubusercontent.com/WikiTeq/mediawiki-pages-ResourceDirectory/master/page-exchange.json';
```
* Navigate to Special:Packages and install the package

# Usage
Navigate to `Form:Resource` to start adding resources. Necessary links for data query and filtering will be added automatically.

# Main data structure
* Resource URL
* Resource type
* Resource name
* Resource author
  * Resource author info
* Resource description
* Resource category
* Resource keyword

# Custom dropdowns
The semantic structure and the data input form can be easily extended to use custom sets of values (dropdowns). 

1) First create desired properties of type `Text` and define allowed values using `[[Allows value::...]]` built-in property. (See `Property:Level` as example).
2) Navigate to `Project:Resource custom lists` and list names of your custom properties delimited with a semicolon (`;`), for example:
```php
Level; MyPropertyName; MyOtherPropertyName
```


