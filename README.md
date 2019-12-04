# MLB
A downloading, organizing and parsing of baseball databases

## Required Modules
```python
from datetime import date, timedelta
import wget,time,os,requests,re
from multiprocessing import Pool, Queue, Process
import shutil as sh
```

## Structure
* Designed to imitate bash scripting in a python format
* It is intended to run as a chron job
* It assessess from 2010 all the way to whatever the current date is
* It downloads from the gd2.mlb.com reads in the format and creates a directory if not already there into:

~MLB \ Year \ Month \ Day \ Game ID 

And in every subdirectorry for individual GID's we have
  1. inning_all.xml
  1. players.xml
  1. inning_hit.xml
