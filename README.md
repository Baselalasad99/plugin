# plugin 
<?php
/*
  Plugin Name: Custom Page Template
  Description: A plugin that creates a new custom page with a custom template.
  Version: 1.0
  Author: ChatGPT
*/

add_action( 'admin_menu', 'create_custom_page' );

function create_custom_page() {
  add_menu_page(
    'Custom Page',
    'Custom Page',
    'manage_options',
    'custom-page',
    'display_custom_page',
    'dashicons-admin-page',
    6
  );
}

function display_custom_page() {
  include( 'custom-page-template.php' );
}
