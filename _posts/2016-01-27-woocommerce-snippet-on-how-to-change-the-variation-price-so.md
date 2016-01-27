---
inFeed: true
hasPage: false
inNav: false
isBasedOnUrl: 'https://gist.github.com/7215b1f5edc2207fd129'
inLanguage: null
starred: false
keywords: []
description: ''
datePublished: '2016-01-27T17:47:54.220Z'
dateModified: '2016-01-27T17:47:44.229Z'
title: Woocommerce Snippet on how to change the variation price so it only displays the lowest
author:
  - name: funkysoul
    url: 'https://github.com/funkysoul'
    avatar: 'https://avatars.githubusercontent.com/u/315914?v=3'
authors: []
publisher:
  name: GitHub
  domain: gist.github.com
  url: 'http://github.com'
  favicon: null
sourcePath: _posts/2016-01-27-woocommerce-snippet-on-how-to-change-the-variation-price-so.md
published: true
_type: Code
_context: 'http://schema.org'

---
add&lowbar;filter&lpar;'woocommerce&lowbar;variable&lowbar;price&lowbar;html'&comma; 'custom&lowbar;variation&lowbar;price'&comma; 10&comma; 2&rpar;&semi;&NewLine;function custom&lowbar;variation&lowbar;price&lpar; &dollar;price&comma; &dollar;product &rpar; &lcub;&NewLine;&Tab;&dollar;price &equals; ''&semi;&NewLine;&Tab;if &lpar; &excl;&dollar;product->min&lowbar;variation&lowbar;price &vert;&vert; &dollar;product->min&lowbar;variation&lowbar;price &excl;&equals;&equals; &dollar;product->max&lowbar;variation&lowbar;price &rpar; &dollar;price &period;&equals; '<span class&equals;"from">' &period; &lowbar;x&lpar;'Ab&nbsp&semi;'&comma; 'min&lowbar;price'&comma; 'woocommerce'&rpar; &period; ' <&sol;span>'&semi;&NewLine;&Tab;&dollar;price &period;&equals; woocommerce&lowbar;price&lpar;&dollar;product->min&lowbar;variation&lowbar;price&rpar;&semi;&NewLine;&Tab;return &dollar;price&semi;&NewLine;&rcub;