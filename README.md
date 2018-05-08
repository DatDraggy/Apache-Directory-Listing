# Apache-Directory-Listing
'Apache Directory Listing' is a theme inspired from [Apaxy](https://github.com/AdamWhitcroft/Apaxy) which uses Apache's `mod_autoindex` module.  
Edited by DatDraggy for usage without .htaccess

# Usage
* Download and copy `directory-listing` to `/usr/share/apache2/`
* In `/etc/apache2/apache2.conf` add following at the bottom: 
````
Alias "/directory-listing" "/usr/share/apache2/directory-listing"
<Directory /usr/share/apache2/directory-listing>
  Options -Indexes
  Order allow,deny
  allow from all
</Directory>
````
* This will tell apache that http://your-domain.com/directory-listing is where the browser can find the files to generate the listing and that it's accessible.
* Take a look at the autoindex.conf file and either edit yours (`/etc/apache2/mods-available/autoindex.conf`) or replace it with this one.
* Enable the autoindex module: `a2enmod autoindex`

# Themes
The theme is included with two css files for grid(`grid.css`) and normal(`table.css`) for table styled indexing.

Just change the `{VIEW}` in `.htaccess` to either `grid` or `table`.

You can add your custom code in the `header.html` and `footer.html`.

### Grid style:  
![grid](https://cloud.githubusercontent.com/assets/12368291/19376773/8444eaa6-91fe-11e6-9a1e-d233553191a6.png)  

### Table style:  
![table](https://cloud.githubusercontent.com/assets/12368291/19376783/951cc542-91fe-11e6-91d1-4a41b7880f7f.png)  

## Credits
Icons referenced from [File Types Icons Set](http://uifest.com/product/file-types-icons-set).
