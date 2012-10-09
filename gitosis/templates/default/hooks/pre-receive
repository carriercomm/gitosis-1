#!/usr/bin/env python

import urllib2
import os
import sys


tsuru_host = os.environ.get("TSURU_HOST", "")
app_name = os.getcwd().split("/")[-1].replace(".git", "")
timeout = 1800

f = urllib2.urlopen("{0}/apps/{1}/avaliable".format(tsuru_host, app_name), timeout=timeout)
if f.getcode() != 200:
    print f.read()
    sys.exit(1)
