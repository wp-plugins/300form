=== Plugin Name ===
Contributors: paddelboot
Tags: form, validation
Requires at least: 3.3.2
Tested up to: 3.3.2
Stable tag: 0.2a
License: GPLv2 or later
License URI: http://www.gnu.org/licenses/gpl-2.0.html

Like the spartans at Thermopylae, these 300 lines of code are meant to protect your forms from malicious invaders. 

I do not claim this code to be complete yet, as it is an alpha version. Before using it in your live site, please do some testing.

== Description ==

Less is more: use this simple plugin to validate your forms. Use regular expressions to match user input against. No need to install huge plugins to validate your forms. Also supports dynamic forms. This plugin is there for validation, to build the actual form, you still have to do the coding.


== Installation ==

1. Upload `300form.php` to the `/wp-content/plugins/` directory
2. Activate the plugin through the 'Plugins' menu in WordPress
3. Get a 'form' class instance. See the files 'page-300form.php' and 'template.php' for example usage.


Optional:

1. Copy the 'page-300form.php' to your theme folder
2. Create a page in the editor using '300form-example' as a template
3. Access the example form in the frontend

== Changelog ==

0.1a
- First version

0.2a
- Added support for dynamic forms


== Upgrade Notice ==

0.2a
- You can now validate dynamic forms, too. I noticed that some of the most popular form plugins cannot do this, which was one of the reasons to write this code.

== Arbitrary section ==

Please leave feedback, bug reports or comments at https://github.com/paddelboot/300form