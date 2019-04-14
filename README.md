<p align="center">
<a href="https://rtcamp.com/?ref=amp-admanager-repo" target="_blank"><img width="200"src="https://rtcamp.com/wp-content/uploads/2018/04/rtcamp-logo-1.svg"></a>
</p>

# AMP AdManager 0.2
AMP ads for all WordPress sites (AMP and Non-AMP). 
This plugin generates `<amp-ad>` code for your ads with breakpoints for responsive display of ads using `min` and `max` attributes.
Works without AMP plugin as well for Non-AMP pages. 

**Contributors:** [rtCamp](https://github.com/rtCamp/), [Vishal Dodiya](https://github.com/vishaldodiya), [Pradeep Sonawane](https://github.com/pradeep910)

**Tags:** [amp](https://wordpress.org/plugins/tags/amp), [mobile](https://wordpress.org/plugins/tags/mobile)
**Requires at least:** 4.9  
**Tested up to:** 5.1  
**License:** [GPLv2 or later](http://www.gnu.org/licenses/gpl-2.0.html)  
**Requires PHP:** 5.4+

# Setup
1. Set network/publisher id in the plugin settings. `Dashboard > AMP AdManager`
2. Select `Load AMP Resources for Non-AMP site` to load `amp-runtime` and `amp-boilerplate` css.

## Usage

#### As Shortcode

```
[ampad width="<slot-width>" height="<slot-height>" 
ad-unit="<ad-unit-name>" min="" max="499" 
sizes="320x50,300x100,300x50" 
custom-targeting="key1:value1, key2:value2"]
```

#### In Template

```php
$attr = [
	'width'     => '<slot-width>',
	'height'    => '<slot-height>',
	'ad-unit'   => '<ad-unit-name>',
	'min'       => '',
	'max'       => '499',
	'sizes'     => '320x50,300x100',
	'layout'    => 'responsive',
	'custom-targeting' => 'key1:value1, key2:value2'
];

AMP_AdManager\AMP_AdManager::get_amp_ad( $attr, true );
```

## Development Flow

* Create new branch from 'master'.
* Name it appropriately, i.e., `feature/GH-<issue-number>-<name>`,`<context>/GH-<issue-number>-<what_it_is>`.
* Create PR against `master`.
* Request review for your changes and get approvals.

## Authors

* **Pradeep Sonawane**
* **Vishal Dodiya**

## Change Log

### v0.2 (14-04-2016)
* Fix shortcode attributes function.
* Add support for user defined targeting with custom-targeting attribute in [ampad]. 
* Type casting for Domain variable.
* Add layout attribute in shortcode for <amp-ad> layout support.

### v0.1
* Basic plugin with ampad shortcode.