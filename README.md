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
