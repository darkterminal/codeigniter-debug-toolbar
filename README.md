CodeIgniter Debug Toolbar
=========================

This is a modified version of the original debug toolbar for CodeIgniter ported from Kohana
Version 0.2.1 (ready for CodeIgniter 2.0-dev)


Copyright 
---------

- based on Kohana Debug Toolbar by Aaron Forsander (http://pifantastic.com/kohana-debug-toolbar/)
- 0.1 ported to CodeIgniter by quark (gothic.quark@gmail.com)
- 0.2 additions by Kon Wilms (konfoo@gmail.com)
- 0.2.1 addition (CI2 compatibility) by michalsn

Installation
-------------

- copy assets folder to webroot
- copy all other content to respective application subdirectories
- enable hooks in application config
- add the following to config/hooks config:
  $hook['display_override'] = array(
    'class' => 'debug_toolbar',
    'function' => 'render',
    'filename' => 'debug_toolbar.php',
    'filepath' => 'hooks'
  );
- configure the config/debug_toolbar config

Additions/Changes
-----------------

- config files are generically parsed for all contents
- matchbox config files are supported and are listed as modules:/name/config
- menu graphic changed 
- some js/css modifications taken from the kohana debug_toolbar (alignment)
- added ability to list files called
- debug bar can be enabled if hidden with a debug_key passed as a $_GET parameter
- changed all names to debug_toolbar to simplify maintenance 
- assets moved and categorized 

Debug_key Functionality
----------------------- 

- edit the debug_toolbar config, set render to FALSE, set a key, and modify the following):
- edit the application config
  - $config['uri_protocol'] = "PATH_INFO";
  - $config['enable_query_strings'] = TRUE;