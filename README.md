# GoogleTagManager
Google Tag Manager: WordPress (Code Snippets Plugin)

This PHP code allows you to insert Google Tag Manager Code Snippets into your WordPress site using the Code Snippets plugin. You can choose to place the snippets in the Header or Footer section. The Footer option is recommended for better Page Speed Performance. Replace the placeholders with your own Google Tag Manager code.

// Add GTM code to the head section
add_action( 'wp_head', function () { ?>
// Paste your GTM code here
<?php }  ); 

// Add GTM code to the footer section
add_action( 'wp_footer', function () { ?>
// Paste your GTM code here
<?php }  ); 

Alternative 1: 

Editing the header.php File
No Code Snippets plugin? You can also edit the header.php file of your WordPress theme and paste the GTM code snippets there. However, this method requires you to use a child theme to avoid losing your changes when updating your theme. You can learn how to create a child theme here: https://developer.wordpress.org/themes/advanced-topics/child-themes/

To edit the header.php file, follow these steps:

Copy the header.php file from your parent theme folder and paste it in your child theme folder.
Open the header.php file in your child theme folder and locate the <head> and <body> tags.
Paste the first GTM code snippet in the <head> section as high as possible.
Paste the second GTM code snippet right after the opening <body> tag.
Save and upload the header.php file to your child theme folder.

Alternative 2:
Use a custom function in your functions.php file and hook it to the wp_head and wp_body_open actions. This adds the code snippets dynamically without editing the header.php file. Use a child theme for this method to avoid losing your changes when updating your theme.

For a custom function, follow these steps:

Copy the functions.php file from your parent theme folder and paste it in your child theme folder.
Open the functions.php file in your child theme folder and add the following code at the end of the file:

// Add GTM code to the head section
  function add_gtm_head() {
  ?>
  // Paste your GTM code here
  <?php
  }
add_action( 'wp_head', 'add_gtm_head' );

// Add GTM code to the footer section
  function add_gtm_body() {
  ?>
  // Paste your GTM code here
  <?php
  }

add_action( 'wp_body_open', 'add_gtm_body' );


Replace the placeholders with your GTM code snippets.
Save and upload the functions.php file to your child theme folder.

Verify Google Tag Manager is working correctly using the Tag Assistant Chrome extension or view the source code of the page.
