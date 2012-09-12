# ![Creative Principle](http://creativeprinciple.com.au/logo2.png)
# Apache Expires Headers


	# 1 YEAR
	<FilesMatch "\.(flv|ico|pdf|avi|mov|ppt|doc|mp3|wmv|wav)$">
	Header set Cache-Control "max-age=29030400, public"
	</FilesMatch>
	 
	# 1 WEEK
	<FilesMatch "\.(jpg|jpeg|png|gif|swf)$">
	Header set Cache-Control "max-age=604800, public"
	</FilesMatch>
	 
	# 3 HOUR
	<FilesMatch "\.(txt|xml|js|css)$">
	Header set Cache-Control "max-age=10800"
	</FilesMatch>
	 
	# NEVER CACHE - notice the extra directives
	<FilesMatch "\.(html|htm|php|cgi|pl)$">
	Header set Cache-Control "max-age=0, private, no-store, no-cache, must-revalidate"
	</FilesMatch>

## htaccess time cheatsheet 
	#      300   5 MIN
	#      600  10 MIN
	#      900  15 MIN
	#     1800  30 MIN
	#     2700  45 MIN
	#     3600   1 HR
	#     7200   2 HR
	#    10800   3 HR
	#    14400   4 HR
	#    18000   5 HR
	#    36000  10 HR
	#    39600  11 HR
	#    43200  12 HR
	#    46800  13 HR
	#    50400  14 HR
	#    54000  15 HR
	#    86400   1 DAY
	#   172800   2 DAY
	#   259200   3 DAY
	#   345600   4 DAY
	#   432000   5 DAY
	#   518400   6 DAY
	#   604800   1 WEEK
	#  1209600   2 WEEK
	#  1814400   3 WEEK
	#  2419200   4 WEEK
	#  4838400   2 MONTH
	#  7257600   3 MONTH
	#  9676800   4 MONTH
	# 12096000   5 MONTH
	# 14515200   6 MONTH
	# 16934400   7 MONTH
	# 19353600   8 MONTH
	# 21772800   9 MONTH
	# 24192000  10 MONTH
	# 26611200  11 MONTH
	# 29030400  12 MONTH	
	
	
## Resources  
* http://httpd.apache.org/docs/2.2/mod/mod_expires.html
* http://www.askapache.com/hacking/speed-site-caching-cache-control.html