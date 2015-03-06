# Downloadable
Wordpress plugin that allows you to create download pages only by uploading the files to the FTP server.

# How to install
Just git clone this repository into your `wp-content/plugins` directory and everything should work.
The final directory structure should be:
```
wp-content
|- plugins
  |- downloadable
     |- downloadable.php
     |- img
```

# How to use this plugin
This plugin is a shortcode only plugin. Here are two examples how to use this plugin in a page or blog content:

```
[downloadable path="downloadable" max_files_in_dir="10" depth="3" include_dirs="Dir to include,Otherdir"]
[downloadable path="downloadable" max_files_in_dir="10" depth="3" exclude_dirs="exclude-dir,exclude-dir2"]
```
