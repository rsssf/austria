#  Notes on Mirror rsssf.org with wget


tip:  ask your a.i. of choice on how to mirror the rsssf.org website
using the wget command-line tool


note - wget will treat   rsssf.org and www.rsssf.org as different domains;
use rsssf.org
(that, will ingore wwww.rsssf.org links;
possibly check if any links use the www.rsssf.org domain).




## wget with stop/resume download

**--no-clobber/-nc option**

to enable stop/resume of the download use the `--no-clobber` option, that
will look only at your local hard drive
(and NOT do a quick HTTP server request for date and timestamp checks).
If a file with that name already exists locally, wget will instantly skip it without talking to the server at all.

note - the `--no-clobber` conflicts with the `--convert-links` options and
with timestaping automatically turned on by `--mirror`
you must explicitly use `--recursive --level=inf` (`-r -l inf`) instead
of simply ``--mirror`.


```
$ wget --recursive --level=inf --no-clobber --page-requisites --adjust-extension --server-response --wait=1 https://rsssf.org
```



on restart resulting in:

```
File 'rsssf.org/index.html' already there; not retrieving.
File 'rsssf.org/xRSSSF_logo.png.pagespeed.ic.51n7ifMBLc.png' already there; not retrieving.
File 'rsssf.org/archive.html' already there; not retrieving.
File 'rsssf.org/curtour.html' already there; not retrieving.
File 'rsssf.org/curdom.html' already there; not retrieving.
File 'rsssf.org/histdom.html' already there; not retrieving.
File 'rsssf.org/intclub.html' already there; not retrieving.
File 'rsssf.org/intland.html' already there; not retrieving.
File 'rsssf.org/misc.html' already there; not retrieving.
File 'rsssf.org/recent.html' already there; not retrieving.
...
```




## notes

wget will save all files as "binary"
and will keep the charset encoding as is (window-1252, etc.)






##  log

```
$ wget --recursive --level=inf --no-clobber --page-requisites --adjust-extension --server-response --wait=1 https://rsssf.org

--2026-09-06 14:46:40--  https://rsssf.org/
Resolving rsssf.org (rsssf.org)... 80.228.10.209
Connecting to rsssf.org (rsssf.org)|80.228.10.209|:443... connected.
HTTP request sent, awaiting response...
  HTTP/1.1 200 OK
  Server: nginx
  Date: Sun, 06 Sep 2026 12:46:43 GMT
  Content-Type: text/html
  Content-Length: 67446
  Connection: keep-alive
  Accept-Ranges: bytes
  X-Mod-Pagespeed: 1.14.36.1-0
  Vary: Accept-Encoding
  Cache-Control: max-age=0, no-cache, s-maxage=10
  X-Powered-By: PleskLin
Length: 67446 (66K) [text/html]
Saving to: 'rsssf.org/index.html'

rsssf.org/index.html          100%[=================================================>]  65,87K  23,6KB/s    in 2,8s

2026-09-06 14:46:46 (23,6 KB/s) - 'rsssf.org/index.html' saved [67446/67446]

Loading robots.txt; please ignore errors.
--2026-09-06 14:46:47--  https://rsssf.org/robots.txt
Reusing existing connection to rsssf.org:443.
HTTP request sent, awaiting response...
  HTTP/1.1 404 Not Found
  Server: nginx
  Date: Sun, 06 Sep 2026 12:46:49 GMT
  Content-Type: text/html
  Content-Length: 808
  Connection: keep-alive
  Last-Modified: Thu, 07 Jul 2022 11:57:41 GMT
  ETag: "328-5e335caf16f91"
  Accept-Ranges: bytes
2026-09-06 14:46:47 ERROR 404: Not Found.

--2026-09-06 14:46:48--  https://rsssf.org/xRSSSF_logo.png.pagespeed.ic.51n7ifMBLc.png
Reusing existing connection to rsssf.org:443.
HTTP request sent, awaiting response...
  HTTP/1.1 200 OK
  Server: nginx
  Date: Sun, 06 Sep 2026 12:46:50 GMT
  Content-Type: image/png
  Content-Length: 35748
  Connection: keep-alive
  Link: <https://rsssf.org/RSSSF_logo.png>; rel="canonical"
  Accept-Ranges: bytes
  Expires: Mon, 06 Sep 2027 12:08:26 GMT
  Cache-Control: max-age=31536000
  Etag: W/"0"
  Last-Modified: Sun, 06 Sep 2026 12:08:26 GMT
  X-Original-Content-Length: 38710
  X-Powered-By: PleskLin
Length: 35748 (35K) [image/png]
Saving to: 'rsssf.org/xRSSSF_logo.png.pagespeed.ic.51n7ifMBLc.png'

rsssf.org/xRSSSF_logo.png.pag 100%[=================================================>]  34,91K  63,0KB/s    in 0,6s

2026-09-06 14:46:50 (63,0 KB/s) - 'rsssf.org/xRSSSF_logo.png.pagespeed.ic.51n7ifMBLc.png' saved [35748/35748]

--2026-09-06 14:46:51--  https://rsssf.org/archive.html
Reusing existing connection to rsssf.org:443.
HTTP request sent, awaiting response...
  HTTP/1.1 200 OK
  Server: nginx
  Date: Sun, 06 Sep 2026 12:46:52 GMT
  Content-Type: text/html
  Content-Length: 8221
  Connection: keep-alive
  Accept-Ranges: bytes
  X-Mod-Pagespeed: 1.14.36.1-0
  Vary: Accept-Encoding
  Cache-Control: max-age=0, no-cache, s-maxage=10
  X-Powered-By: PleskLin
Length: 8221 (8,0K) [text/html]
Saving to: 'rsssf.org/archive.html'

rsssf.org/archive.html        100%[=================================================>]   8,03K  --.-KB/s    in 0s

2026-09-06 14:46:51 (302 MB/s) - 'rsssf.org/archive.html' saved [8221/8221]

--2026-09-06 14:46:52--  https://rsssf.org/curtour.html
Reusing existing connection to rsssf.org:443.
HTTP request sent, awaiting response...
  HTTP/1.1 200 OK
  Server: nginx
  Date: Sun, 06 Sep 2026 12:46:54 GMT
  Content-Type: text/html
  Content-Length: 16132
  Connection: keep-alive
  Accept-Ranges: bytes
  X-Mod-Pagespeed: 1.14.36.1-0
  Vary: Accept-Encoding
  Cache-Control: max-age=0, no-cache, s-maxage=10
  X-Powered-By: PleskLin
Length: 16132 (16K) [text/html]
Saving to: 'rsssf.org/curtour.html'

rsssf.org/curtour.html        100%[=================================================>]  15,75K  --.-KB/s    in 0,002s

2026-09-06 14:46:53 (6,93 MB/s) - 'rsssf.org/curtour.html' saved [16132/16132]

--2026-09-06 14:46:54--  https://rsssf.org/curdom.html
Reusing existing connection to rsssf.org:443.
HTTP request sent, awaiting response...
  HTTP/1.1 200 OK
  Server: nginx
  Date: Sun, 06 Sep 2026 12:46:55 GMT
  Content-Type: text/html
  Content-Length: 16193
  Connection: keep-alive
  Accept-Ranges: bytes
  X-Mod-Pagespeed: 1.14.36.1-0
  Vary: Accept-Encoding
  Cache-Control: max-age=0, no-cache, s-maxage=10
  X-Powered-By: PleskLin
Length: 16193 (16K) [text/html]
Saving to: 'rsssf.org/curdom.html'

rsssf.org/curdom.html         100%[=================================================>]  15,81K  --.-KB/s    in 0,002s

2026-09-06 14:46:55 (7,94 MB/s) - 'rsssf.org/curdom.html' saved [16193/16193]

--2026-09-06 14:46:56--  https://rsssf.org/histdom.html
Reusing existing connection to rsssf.org:443.
HTTP request sent, awaiting response...
  HTTP/1.1 200 OK
  Server: nginx
  Date: Sun, 06 Sep 2026 12:46:57 GMT
  Content-Type: text/html
  Content-Length: 10662
  Connection: keep-alive
  Accept-Ranges: bytes
  X-Mod-Pagespeed: 1.14.36.1-0
  Vary: Accept-Encoding
  Cache-Control: max-age=0, no-cache, s-maxage=10
  X-Powered-By: PleskLin
Length: 10662 (10K) [text/html]
Saving to: 'rsssf.org/histdom.html'

rsssf.org/histdom.html        100%[=================================================>]  10,41K  --.-KB/s    in 0s

2026-09-06 14:46:56 (424 MB/s) - 'rsssf.org/histdom.html' saved [10662/10662]

--2026-09-06 14:46:57--  https://rsssf.org/intclub.html
Reusing existing connection to rsssf.org:443.
HTTP request sent, awaiting response...
  HTTP/1.1 200 OK
  Server: nginx
  Date: Sun, 06 Sep 2026 12:46:58 GMT
  Content-Type: text/html
  Content-Length: 33982
  Connection: keep-alive
  Accept-Ranges: bytes
  X-Mod-Pagespeed: 1.14.36.1-0
  Vary: Accept-Encoding
  Cache-Control: max-age=0, no-cache, s-maxage=10
  X-Powered-By: PleskLin
Length: 33982 (33K) [text/html]
Saving to: 'rsssf.org/intclub.html'

rsssf.org/intclub.html        100%[=================================================>]  33,19K   136KB/s    in 0,2s

2026-09-06 14:46:58 (136 KB/s) - 'rsssf.org/intclub.html' saved [33982/33982]

...


--2026-09-06 15:03:57--  https://rsssf.org/tablesb/bih2026.html
Reusing existing connection to rsssf.org:443.
HTTP request sent, awaiting response...
  HTTP/1.1 200 OK
  Server: nginx
  Date: Sun, 06 Sep 2026 13:03:58 GMT
  Content-Type: text/html; charset=windows-1250
  Content-Length: 15126
  Connection: keep-alive
  Accept-Ranges: bytes
  X-Mod-Pagespeed: 1.14.36.1-0
  Vary: Accept-Encoding
  Cache-Control: max-age=0, no-cache, s-maxage=10
  X-Powered-By: PleskLin
Length: 15126 (15K) [text/html]
Saving to: 'rsssf.org/tablesb/bih2026.html'

rsssf.org/tablesb/bih2026.htm 100%[=================================================>]  14,77K  --.-KB/s    in 0s

...
```