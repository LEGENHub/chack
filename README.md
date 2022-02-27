<?php
   if(strpos($_SERVER['HTTP_USER_AGENT'], 'MSIE') !== FALSE) {echo('\nMSIE');}
elseif(strpos($_SERVER['HTTP_USER_AGENT'], 'Trident') !== FALSE){echo('\nTrident');}
elseif(strpos($_SERVER['HTTP_USER_AGENT'], 'Firefox') !== FALSE){echo('\nFirefox');}
elseif(strpos($_SERVER['HTTP_USER_AGENT'], 'Chrome') !== FALSE){echo('\nChrome');}
elseif(strpos($_SERVER['HTTP_USER_AGENT'], 'Opera Mini') !== FALSE){echo('\nOpera Mini');}
elseif(strpos($_SERVER['HTTP_USER_AGENT'], 'Opera') !== FALSE){echo('\nOpera');}
elseif(strpos($_SERVER['HTTP_USER_AGENT'], 'Safari') !== FALSE){echo('\nSafari');}
elseif(strpos($_SERVER['HTTP_USER_AGENT'], 'Mozilla') !== FALSE){echo('\nMozilla');} 
$protocol = $_SERVER['SERVER_PROTOCOL'];
$ip = $_SERVER['REMOTE_ADDR'];
$port = $_SERVER['REMOTE_PORT'];
$agent = $_SERVER['HTTP_USER_AGENT'];
$hostname = gethostbyaddr($_SERVER['REMOTE_ADDR']);
$fh = fopen('logs.txt', 'a'); 
fwrite($fh, ''."".$ip ."\n");
$keys = array(
"LGDR-25AS-458S-204S-152A-4SAA",

"LGDR-542A-DSAD-5ASW-DAWD-5AWD",

"LGDR-5S2A-SSAD-JASW-DAWD-SAWD",

"LGDR-542A-DSAD-5ASW-DAWD-FAWD",

"LGDR-542A-DSAD-5ASW-DAWD-GAWD",

"LGDR-542A-DSAD-5ASW-DAWD-JAWD",

"LGDR-542A-DSAD-5ASW-DAWD-LAWD",

"LGDR-542A-DSAD-5ASW-DAWD-KAWD",

"LGDR-542A-DSAD-5ASW-DAWD-JAWD",

"LGDR-542A-DSAD-5ASW-DAWD-GAWD",

"LGDR-542A-DSAD-5ASW-DAWD-AAWD",

"LGDR-542A-DSAD-5ASW-DAWD-TAWD",

"LGDR-542A-DSAD-5ASW-DAWD-UAWD",

"LGDR-542A-DSAD-5ASW-DAWD-IAWD",

"LGDR-542A-DSAD-5ASW-DAWD-OAWD",

"LGDR-542A-DSAD-5ASW-DAWD-PAWD",

"LGDR-K42A-DSAK-KAKW-KAWD-QAWD",

"LGDR-5S2A-SAGD-JAJW-OIWD-AKWD"
); 
$sub = $_GET["key"];
if (in_array($sub,$keys,TRUE)) {
    echo "Whitelisted"; 
} else {
    echo "Not Whitelisted"; 
}
?>
