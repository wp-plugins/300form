=== Plugin Name ===
Contributors: paddelboot
Tags: form, validation
Requires at least: 3.3.2
Tested up to: 3.3.2
Stable tag: 0.2a
License: GPLv2 or later
License URI: http://www.gnu.org/licenses/gpl-2.0.html

Like the Spartans at Thermopylae, these 300 lines of code are meant to protect your forms from malicious invaders. 

== Description ==

<h4>Less is more</h4> 
Use this simple plugin to validate your forms. Use regular expressions to match user input against. No need to install huge plugins to validate your forms. This plugin is there for validation, to build the actual form, you still have to do the coding.

<h4>Features</h4>
<ul>
<li>Obligatory fields</li>
<li>Patterns matching</li>
<li>Support for dynamic forms</li>
</ul>

I do not claim this code to be complete yet, as it is an alpha version. Before using it in your live site, please do some testing.

== Installation ==

<h3>How to install</h3>

1. Upload `300form.php` to the `/wp-content/plugins/` directory
2. Activate the plugin through the 'Plugins' menu in WordPress
3. Get a 'form' class instance. See the files 'page-300form.php' and 'template.php' for example usage.


<h3>Optional:</h3>

1. Copy the 'page-300form.php' to your theme folder
2. Create a page in the editor using '300form-example' as a template
3. Access the example form in the frontend

<h3>How to use (example):</h3>

$form = new form();
$form->required = array( 'form_name', 'form_place' );
$form->pattern = array( 'form_name' => '!^[a-zA-Z]$!', 'form_place' => '!^[a-zA-Z]$!' );
$form->process( $_POST );
$data = $form->processed_data;

*your_form_template*
<input type="text" name="form_name" placeholder="Your Name" value="<?php $form->data( 'form_name' ); ?>" />
<span style="color:red"><?php $form->hint( 'form_name' ); ?></span>
*/your_form_template*

<h3>API</h3>
<ul>
<li>$required | array containing names of required form fields</li>
<li>$pattern | array containing key/value pairs of field names and their corresponding regular expressions</li>
<li>$process( $data ) | function that starts the validation process. Must be passed REQUEST data as first parameter</li>
<li>$processed_data | If all validation checks are passed, this var contains the validated REQUEST data</li> 
<li>$data( $handler ) | wrapper for get_data( $handler ). Outputs the value entered in the $handler form field</li>
<li>$hint( $handler ) | wrapper for get_hint( $handler ). Outputs the form field's hint</li>
</ul>

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