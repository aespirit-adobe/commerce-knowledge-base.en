---
title: 'PWA Studio: Browser displays “Cannot proxy to“ error'
description: This topic discusses a solution when your web browser displays a "*Cannot proxy to*" and the console displays an
exl-id: de689633-34b8-4a25-bbd0-a58742c4d03c
---
# PWA Studio: Browser displays “Cannot proxy to“ error

This topic discusses a solution when your web browser displays a "*Cannot proxy to*" and the console displays an

```clike
ENOTFOUND
```

error when using Progressive Web App (PWA) Studio for Adobe Commerce.

## Affected products and versions

* PWA Studio for Adobe Commerce

## Issue

<u>Step to reproduce</u>:

* Load your Adobe Commerce store in a browser.

<u>Expected result</u>:

* The Adobe Commerce store loads normally in your browser.

<u>Actual result</u>:

* Your web browser displays the “*Cannot proxy to*“ error and the console displays an error like:

```clike
    ENOTFOUND
```


## Cause

NodeJS cannot resolve the hostname of your Adobe Commerce store.

## Solution

1. Make sure your Adobe Commerce store loads in more than one web browser.
1. If you are running a local DNS server or VPN, add an entry to your hostfile (located in `/etc/hosts`) and manually map this domain ([Generic instructions on hostfile editing](https://linuxize.com/post/how-to-edit-your-hosts-file/)) so NodeJS can resolve it.

## Related reading

* [PWA Studio for Adobe Commerce Documentation](https://magento.github.io/pwa-studio/)
* [Tools and libraries](https://magento.github.io/pwa-studio/technologies/tools-libraries/)
