# Rapid Refresh

#### Rapid Refresh allows you to preview any URL on large number of mobile devices simultaneously. Just enter a URL, hit Enter, and new URL gets automatically loaded on each device. Works on platforms like Android, Blackberry, iOS, Maemo, Meego, Symbian, Windows Phone and WebOS. 

##### Rapid Refresh is based on [Remote Preview](http://viljamis.com/blog/2012/remote-preview/), built by [@viljamis](http://twitter.com/viljamis) for the [Helsinki Device Lab](http://devicelab.fi).

Rapid Refresh works by making an ajax call every 1100ms to check if the url in the 'url.txt' file is changed. If it is, the script will then change the src attribute of the iframe and load a new page into it. If there's no changes, the script will just keep polling the url.txt until something changes. Rapid Refresh allows very fast previewing of different URL's to check for possible layout problems, which can then be debugged using various other tools depending on the platform where they occur.

## Basic usage

1. Move all files to a public Dropbox folder/Server/localhost, edit ‘url.txt’, hit Ctrl+S (save…) and wait for devices to refresh. That's all!
2. Bookmark Rapid Refresh to your devices’s home screen for fast & easy application like access later on.
3. If you moved all files to a server or localhost, you can control the devices via web browser by pointing your browser to the directory called /control/.
4. To make the Controller page work, you need to make sure that PHP is enabled on the server and that the url file has necessary write permissions. You should also limit the access to this page somehow as otherwise anyone can go to that url and control the devices.
5. Use ID's to scroll down to a certain point on a page. URL#ID, for example: http://opendevicelab.com/#location


## Browser support

Current alpha version is tested to be working on at least following platforms:

* Android OS 2.1 - 4.1.2 (Default browser + Chrome)
* Blackberry OS 7.0 (Default browser)
* iOS 4.2.1 - 6 (Default browser)
* Mac OS X (Safari, Chrome, Firefox, Opera)
* Maemo 5.0 (Default browser)
* Meego 1.2 (Default browser)
* Symbian 3 (Default browser)
* Symbian Belle (Default browser)
* WebOS 3.0.5 (Default browser)
* Windows Phone 7.5 (Default browser)
* Windows 7 (IE9)

## Known issues

* Pages open inside iframe
	* Google and Yahoo (possibly others) do not allow pages to be shown in iframes.
* You have to write the url with `http(s)://` prefix
* On Windows Phone 7.5 the iframe's src attribute can't be empty
* On Android 4.0.4, when using Chrome browser, a fixed positioned element inside iframe seems to prevent the whole page's scrolling
* On Android 2.1, when using default browser, the page stops auto updating after user scrolls down



