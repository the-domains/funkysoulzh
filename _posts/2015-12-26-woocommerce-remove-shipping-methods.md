---
inFeed: true
hasPage: true
inNav: false
inLanguage: null
starred: false
keywords: []
description: A short tutorial on how to remove shipping methods when free shipping is available
datePublished: '2015-12-26T17:26:05.607Z'
dateModified: '2015-12-26T17:25:52.466Z'
title: WooCommerce - Remove Shipping Methods
author: []
authors: []
publisher:
  name: null
  domain: null
  url: null
  favicon: null
sourcePath: _posts/2015-12-26-woocommerce-remove-shipping-methods.md
published: true
url: woocommerce-remove-shipping-methods/index.html
_type: Article

---
So you probably landed on my site because you ripping your hair out since hours and you just need to ALL shipping methods when you enabled Free Shipping.

Actually that sounds very complicated, but it isn't (cough cough)

add\_filter( 'woocommerce\_available\_shipping\_methods', 'hide\_all\_shipping\_when\_free\_is\_available' , 10, 1 );
function hide\_all\_shipping\_when\_free\_is\_available( $available\_methods ) {
if( isset( $available\_methods\['free\_shipping'\] ) ) :
// Get Free Shipping array into a new array
$freeshipping = array();
$freeshipping = $available\_methods\['free\_shipping'\];
// Empty the $available\_methods array
unset( $available\_methods );
// Add Free Shipping back into $avaialble\_methods
$available\_methods = array();
$available\_methods\[\] = $freeshipping;
endif;
return $available\_methods;
}