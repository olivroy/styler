---
editor_options: 
  markdown: 
    wrap: 79
---

This is a release requested by the CRAN team to delete the population of the 
user's cache while building vignettes.


## Test environments

-   ubuntu 20.04 (on GitHub Actions): R devel, R 4.3.0, R 4.2.1, 4.1.2, R 4.0.5, 
    R 3.6
-   Windows Server 10 (on GitHub Actions): R devel, R 4.3.0, R 4.2.1, R 4.1.2, 
    R 3.6.
-   win-builder: R devel

## R CMD check results

0 ERRORS \| 0 WARNINGS \| 1 NOTES

The note was generated on winbuilder when incoming checks were enabled only and
contained many blocks like this:

    Found the following (possibly) invalid URLs:
      URL: https://github.com/ropensci/drake
        From: inst/doc/third-party-integrations.html
              NEWS.md
        Status: 429
        Message: Too Many Requests

It seems my package contains many URLs to GitHub and their rate limit prevents
the checking of all of them. I confirm that all URLs in my package are
compliant with the requirements of CRAN.

## Downstream Dependencies

I also ran R CMD check on all 39 downstream dependencies of styler using the
revdepcheck package.

All of them finished R CMD CHECK with the same number of ERRORS, WARNINGS and 
NOTES.
