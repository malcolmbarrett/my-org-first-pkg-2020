---
title: Install R packages
author: ''
date: "2020-01-23"
slug: packages
categories: []
tags: []
linktitle: "Install R packages"
menu:
  pre:
    parent: "Local setup"
    weight: 3
toc: yes
type: docs
---



You can download all the R packages we will need as well as download the course materials using the course R package, which you can install from GitHub using the remotes package.


```r
# if needed:
# install.packages("remotes")
remotes::install_github("malcolmbarrett/firstrpkg")
```

The installation of **RMariaDB**, which we'll use on day 2, requires the installation of system libraries. The names of the libraries and their method of installation depend on the system:

### Debian or Ubuntu
`sudo apt-get install -y libmysqlclient-dev`
`sudo apt-get install -y libmariadb-client-lgpl-dev`

### Fedora, CentOS, or RHEL
`sudo yum install mysql-devel`
`sudo yum install mariadb-devel`

### Mac (Homebrew)
`brew install mysql-connector-c++`
`brew install mariadb-connector-c`

## Download the course materials

Once you've installed the package and RMariaDB, download the workshop materials with

``` r
firstrpkg::install_workshop("path/to/your/computer")
```

Replace "path/to/your/computer" with where on your computer you want the workshop installed.

**Note that the download size of the workshop materials is around 200 MB and may take some time.** 

If you prefer to work with the materials via git, you can just install course package without running `install_workshop()`. You can find the materials on the [course GitHub repository](https://github.com/rstudio-conf-2020/my-org-first-pkg).
