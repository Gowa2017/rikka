# Tencent COS —— Cloud Object Service Plugin

[中文版][version-zh]

Added in version 0.4.0, inner name `tccos`.

## Description

This plugin use Cloud Object Service (COS) of Tencent to store image files.

## Options

You should provide 4 options: APPID, Secret ID, Secret Key and Bucket Name.

First three options should be provided in env var, use key `RIKKA_TENCENT_APPID`, `RIKKA_TENCENT_SECRETID` and `RIKKA_TENCENT_SECRETKEY`.

And the Bucket Name should be specified by the command line option `-bname`.

If you want, you can use option `-bpath` to set the path image will be store to(Notice: The path should already exist).

For example, `-bpath rikka`，will save image in `rikka` folder.

## Notices

As a "Static File Store Server", Tencent COS make browsers download the file when visits file url, instand of preview them.

In other word, if you visit a url of image saved in COS in your browser, it will download the image rather than open a new tab to preview the image. 

But it's ok to use the image url in `src` attr of `image` element, or `background` attr of other elements in HTML, 

If you want change this action, you need to bind COS to your own domain and enable the static weisite option.

Refer: [Tencent COS static website option doc][][tencent-cos-static-website-doc].

## Guide

WIP

[version-zh]: https://github.com/7sDream/rikka/blob/master/plugins/tencent/cos/README.zh.md
[tencent-cos-static-website-doc]: https://www.qcloud.com/doc/product/227/%E9%85%8D%E7%BD%AE%E8%AF%A6%E6%83%85#5-静态网站