# Replace ISPConfig multilanguage index web host file with custom template

## Backup original index files

`$ cd /usr/local/ispconfig/server/conf/index`

`$ sudo tar -cpzvf ../index.tar.gz .`



## Create a new custom html template and fill with desired content

`$ sudo vi standard_index.html_TEMPLATE`

## Replace all standard_index.html_LANGUAGE files with new standard_index.html_TEMPLATE:

`$ sudo find . -type f -name "standard_index.html*" ! -name "*_TEMPLATE" -exec cp standard_index.html_TEMPLATE {} \;`

*All new created hosts will have custom TEMPLATE in the vhost web directory*

---
<mark>A custom template for user_standard_index.html_LANG files can be changed in the same way (take care of {USER_USERNAME} variable)</mark>
