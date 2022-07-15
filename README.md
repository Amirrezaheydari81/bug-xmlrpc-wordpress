## English version
# bug-xmlrpc-wordpress
A new and maybe old bug for hacking the site by sending stations inside the url as a post and how to prevent it

Location File : `public_html > xmlrpc.php`

### Now how do we stop this problem?
##### There are 3 methods

1. Plugin Wordpress : [disable-xml-rpc](https://wordpress.org/plugins/disable-xml-rpc/)
2. Disable XML-RPC Pingbacks with a Plugin : [disable-xml-rpc-pingback](https://wordpress.org/plugins/disable-xml-rpc-pingback/)
3. Configure XML-RPC and REST API Activation with a Plugin : [rest-xmlrpc-data-checker](https://wordpress.org/plugins/rest-xmlrpc-data-checker/)

### How to Disable xmlrpc.php Without a Plugin
##### There are 3 methods
1. Disable xmlrpc.php via a Filter : `add_filter( 'xmlrpc_enabled', '__return_false' );
`
**An option here is to use the xmlrpc_enabled filter to disable xmlrpc.php. Add this function to a plugin and activate it on your site:**
<br/>
2. Disable xmlrpc.php via the .htacess File : `<Files xmlrpc.php>
Order Allow,Deny
Deny from all
</Files>` 
**In your .htaccess file, add this code**
<br/>
3. Have Your Hosting Provider Disable xmlrpc.php : `location ~* ^/xmlrpc.php$ {
return 403;
}`
**snippet of code is automatically added to the Nginx.config file**

##### In the shell folder, I will put a bunch of files that the hacker injected into our server for you to see what she did.

I made a default `.htaccess` security file for you if you want to replace it in your host to increase your security
###### Author: Amirreza Heydari

## Persian version
# bug-xmlrpc-wordpress
یک باگ جدید و شاید قدیمی برای هک سایت با ارسال ایستگاه های داخل url به عنوان پست و نحوه جلوگیری از آن

محل فایل: public_html > xmlrpc.php

### حالا چگونه جلوی این مشکل را بگیریم؟
##### 3 روش وجود دارد

1. افزونه وردپرس: [disable-xml-rpc](https://wordpress.org/plugins/disable-xml-rpc/)
2. Pingback های XML-RPC را با یک افزونه غیرفعال کنید: [disable-xml-rpc-pingback](https://wordpress.org/plugins/disable-xml-rpc-pingback/)
3. فعال‌سازی XML-RPC و REST API را با یک افزونه پیکربندی کنید: [rest-xmlrpc-data-checker](https://wordpress.org/plugins/rest-xmlrpc-data-checker/)

### چگونه xmlrpc.php را بدون پلاگین غیرفعال کنیم
##### 3 روش وجود دارد
1. xmlrpc.php را از طریق فیلتر غیرفعال کنید: `add_filter('xmlrpc_enabled', '__return_false' );
`
**یک گزینه در اینجا استفاده از فیلتر xmlrpc_enabled برای غیرفعال کردن xmlrpc.php است. این تابع را به یک افزونه اضافه کنید و آن را در سایت خود فعال کنید:**

<br/>

2. xmlrpc.php را از طریق فایل .htacess غیرفعال کنید: `<Files xmlrpc.php>
سفارش اجازه، انکار
انکار از همه
</Files>`
**در فایل htaccess خود، این کد را اضافه کنید**

<br/>

3. از ارائه دهنده هاست خود بخواهید xmlrpc.php را غیرفعال کند : `location ~* ^/xmlrpc.php$ {
بازگشت 403;
}`
**قطعه کد به طور خودکار به فایل Nginx.config اضافه می شود**

##### در پوشه shell یکسری از فایل هایی که هکر در سرور ما تزریق کرده بود را برای شما قرار میدم تا ببینید چه کار کرده است
یک فایل پیشفرض امنیتی `.htaccess` برای شما درست کردم اگر دوست داشتید در هاست خود جایگزین کنید تا امنیت شما بالا برود
###### نویسنده : امیررضا حیدری