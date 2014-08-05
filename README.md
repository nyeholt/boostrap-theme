# Bootstrap 3.2.0 theme for SilverStripe

Containing the Slate custom theme. 

## Usage

* Extract to themes/ directory
* Change theme setting in your local config

---
Name: theme_config
---
SSViewer:
  theme: bootstrap-theme


* Add the following to your Page_Controller::init() method

```

	$theme = Config::inst()->get('SSViewer', 'theme');
	Requirements::css('themes/' . $theme . '/css/slate.css');
	Requirements::css('themes/' . $theme . '/css/custom.css');
	
	Requirements::javascript(THIRDPARTY_DIR .'/jquery/jquery.js');
	Requirements::javascript('themes/' . $theme . '/js/bootstrap.js');

```