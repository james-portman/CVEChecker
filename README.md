CVE Checker
===========

This script and (optional, poorly thought out) web interface will check Red Hat's CVE database to retrieve information on what version the issue was fixed via a backport patch. Think [SCAP](http://en.wikipedia.org/wiki/Security_Content_Automation_Protocol), except much less useful.

To use, pipe in a whitespace separated list of CVE references in one of the following forms (for example):

   `python rhsa.py < cvelist.txt`
   `echo "CVE-2001-1002 CVE-2004-4002" | python rhsa.py`

Alternatively launch the web interface with `python web.py`.

Requires:

    * Python >= 2.3 (tested with Python 2.6, CentOS 6)
    * BeautifulSoup
    * SNMP Python libraries (net-snmp-python on CentOS/RHEL)
    
Additionally, for the optional web interface:
    
    * Mako
    * Scrubber
    * CherryPy

Currently working on SNMP integration to query remote servers for version information using SNMPv1 (...yeah, I know). 
