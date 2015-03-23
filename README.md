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

# Resulting downloads
The results are one or more unordered lists for each directory and a list item with the download link for each file in this directory. The plugin searches for an image with the name of the file extension (e.g. `pdf.png` or `mp3.png`). If this image exists, it will be displayed left to the download link.

# Shortcode Parameters

#### `path`
This has to be given and is the root path where your files are located.

#### `depth`
This is the depth of recursion where 1 means only the topmost hierarchy (the path specified). Default is 1.

#### `max_files_in_dir`
This reduces the number of displayed files in each directory. This defaults to -1, which means all files.

#### `exclude_dirs` and `include_dirs`
These parameters are given as a comma seperated list of directory names. If a directory is part of the `exclude_dirs` list, it will be ignored. If it isn't on this list and no `include_dirs` are given, it will be included in the results. If a `include_dirs` parameter is given, it only will be displayed if it is part of this list.
