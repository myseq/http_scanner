# Tool: httphdr_scan
This is a tool (written in Python) to perform quick scan on HTTP version and headers.

Main features include:
 - show HTTP version
 - show HTTP server and version
 - show security HTTP header (verbose)

Other capabilities:
 - show the elapsed time for individual site
 - show the total and real time taken 
 - can scan spcific URL
 - can scan a list of sites from an input file
 - allow to follow [301] redirection
 - always make async connections

# Security HTTP Headers
Got the same idea from https://securityheaders.com/

## Headers
 - Strict-Transport-Security
 - Content-Security-Policy
 - X-Frame-Options
 - X-Content-Type-Options
 - Referrer-Policy
 - Permissions-Policy
 - X-XSS

# Usage
```bash
$ ./main.py -h
usage: main.py [-h] [-u <url> [<url> ...]] [-f <sites.url>] [-r] [-v]

options:
  -h, --help            show this help message and exit
  -u <url> [<url> ...]  Specifying URL
  -f <sites.url>        Specifying input site file
  -r                    Follow HTTP 301 redirection.
  -v                    verbose output
```

## Samples
Below is the sample output, showing the scan of 5 default sites.

![httphdr_scan.py](output.png)
