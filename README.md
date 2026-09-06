# RSSSF Mirror (& Text Corpus)


what?

the goal here is to mirror the rsssf.org site
and prepare a (slightly cleaned-up) text corpus
for an all-in-one download
to help along research and experimentation
with the 40000+ football archive rsssf pages


note - all scripts used are open-source (see [/scripts](https://github.com/rsssf/scripts))
along with documentation to update or start from scratch









The directory structure of the (mirrored) rsssf.org website
(about 40 000+ .html pages):

```
└───rsssf.org                => 66
    ├───bvv                  => 221
    ├───colours              => 220
    ├───ec                   => 190
    ├───engpaul
    │   └───FLA              => 111
    ├───intldetails          => 214
    ├───miscellaneous        => 6053
    ├───nedfer               => 27
    ├───players              => 1943
    ├───rssbest              => 218
    ├───sacups               => 345
    ├───tables               => 580
    ├───tablesa              => 3053
    ├───tablesb              => 1887
    ├───tablesc              => 2333
    ├───tablesd              => 1174
    │   └───dfbcup           => 8
    ├───tablese              => 1407
    ├───tablesf              => 1092
    ├───tablesg              => 1378
    ├───tablesh              => 633
    ├───tablesi              => 1556
    ├───tablesj              => 516
    ├───tablesk              => 951
    ├───tablesl              => 841
    ├───tablesm              => 2206
    ├───tablesn              => 1645
    ├───tableso              => 889
    ├───tablesp              => 1412
    ├───tablesq              => 92
    ├───tablesr              => 894
    ├───tabless              => 2988
    ├───tablest              => 1399
    ├───tablesu              => 767
    ├───tablesv              => 420
    ├───tablesw              => 747
    ├───tablesx              => 22
    ├───tablesy              => 71
    ├───tablesz              => 849
    ├───usadave              => 56
    └───wk94                 => 14
```

There are the a-z (26) `/tables[a-z]` plus the `/tables`
"core" directories
plus about a dozen extras directories:

```
└───rsssf.org    (with /tables* hidden)
    ├───bvv
    ├───colours
    ├───ec
    ├───engpaul
    │   └───FLA
    ├───intldetails
    ├───miscellaneous
    ├───nedfer
    ├───players
    ├───rssbest
    ├───sacups
    ├───usadave
    └───wk94
```




report number of indexed pages:

by type:
- .html
- .pdf
- spreadsheets (.xlsd?)
- images (.jpg)  - incl. scanned documents as images

by (charset) encoding  (only incl. .html):
- windows-1256?
- utf-8
- utf-16le
- ...


report broken links - 404 page not found:







## more

for notes on using the `wget` command-line tool to mirror the rsssf.org website,
see [/wget »](wget)