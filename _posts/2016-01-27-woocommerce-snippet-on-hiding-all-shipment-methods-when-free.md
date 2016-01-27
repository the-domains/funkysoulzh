---
title: Woocommerce Snippet on hiding all shipment methods when free shipping is available
author:
  - name: funkysoul
    url: 'https://github.com/funkysoul'
    avatar: 'https://avatars.githubusercontent.com/u/315914?v=3'
publisher:
  url: 'http://github.com'
  name: GitHub
  domain: gist.github.com
isBasedOnUrl: 'https://gist.github.com/7756a007f861595af7ce'
datePublished: '2016-01-27T17:57:47.274Z'
dateModified: '2016-01-27T17:57:17.572Z'
sourcePath: _posts/2016-01-27-woocommerce-snippet-on-hiding-all-shipment-methods-when-free.md
published: true
inFeed: true
hasPage: false
inNav: false
_type: Code
_context: 'http://schema.org'

---
add&lowbar;filter&lpar; 'woocommerce&lowbar;available&lowbar;shipping&lowbar;methods'&comma; 'hide&lowbar;all&lowbar;shipping&lowbar;when&lowbar;free&lowbar;is&lowbar;available' &comma; 10&comma; 1 &rpar;&semi; &NewLine;function hide&lowbar;all&lowbar;shipping&lowbar;when&lowbar;free&lowbar;is&lowbar;available&lpar; &dollar;available&lowbar;methods &rpar; &lcub; &NewLine;&Tab;if&lpar; isset&lpar; &dollar;available&lowbar;methods&lsqb;'free&lowbar;shipping'&rsqb; &rpar; &rpar; &colon; &NewLine;&Tab;&Tab;&dollar;freeshipping &equals; array&lpar;&rpar;&semi; &dollar;freeshipping &equals; &dollar;available&lowbar;methods&lsqb;'free&lowbar;shipping'&rsqb;&semi; &NewLine;&Tab;&NewLine;&Tab;array unset&lpar; &dollar;available&lowbar;methods &rpar;&semi; &NewLine;&NewLine;&Tab;&dollar;available&lowbar;methods &equals; array&lpar;&rpar;&semi; &NewLine;&Tab;&dollar;available&lowbar;methods&lsqb;&rsqb; &equals; &dollar;freeshipping&semi; &NewLine;&Tab;endif&semi; &NewLine;&Tab;return &dollar;available&lowbar;methods&semi; &NewLine;&rcub;