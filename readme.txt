=== WP Quip ===
Contributors:
Tags: quip, doc
Donate link: https://cloudposse.com/
Requires at least: 4.0
Tested up to: 4.9.2
Requires PHP: 5.6
Stable tag: 1.0
License: GPLv2 or later
License URI: http://www.gnu.org/licenses/gpl-2.0.html

Quip integration for WordPress.
`WP Quip` plugin uses WordPress shortcodes to embed Quip documents into WordPress pages and blog posts.

== Description ==
Quip integration for WordPress


## Introduction

`WP Quip` plugin uses WordPress shortcodes to embed [Quip](https://quip.com/) documents into WordPress pages and blog posts.

https://codex.wordpress.org/Shortcode

https://codex.wordpress.org/Shortcode_API


## Usage

To embed the content of a [Quip](https://quip.com/) document into a WordPress page or blog post, use the `quip` shortcode.

`quip` shortcode accepts two attributes and has the following format:

```
[quip id=\"mWnnAszre3MW\" ttl=7200]
```

where

* `id` (Required) - The ID of the Quip document (_e.g._ https://quip.com/mWnnAszre3MW)

* `ttl` (Optional) - Time-To-Live in seconds.
After the first request to the Quip API, the plugin caches the content of the document (HTML and images) for the specified amount of time (seconds).
All consecutive requests to the same page or blog post will not call the Quip API again but will retrieve the document from the internal cache, making the pages faster.
After the `ttl` expires, the plugin will call the Quip API and cache the result again.
If the `ttl` attribute is not provided, the default value of 7200 seconds (2 hours) is used.
You can change the default value in `Quip Settings` (menu `Settings/WP Quip`).


== Installation ==
1. Upload `wp-quip` folder to the `/wp-content/plugins/` directory

2. Activate the `WP Quip` plugin through the `Plugins` menu in WordPress

3. On `Quip Settings` page (menu `Settings/WP Quip`), you can update the default value for `Time-to-Live`

4. On `Quip Settings` page, enter and save `Quip API Access Token`

NOTE: To generate a Quip API Access Token, visit this page: https://quip.com/dev/token .
Whenever you generate a new token, all previous tokens are automatically invalidated.


== Screenshots ==
1. WP Quip plugin Settings page

== Changelog ==
= 1.0 =
* Initial release.