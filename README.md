ansible-autozone
================

Pulls WWPNs from a Cisco UCS service profiles, and create zone config snippets 

Requires Python 2.7.x, Cisco UCS Python SDK 0.8.3

# Setup

Python 2.7.9 enables certificate validation by default.  Need to edit the UCS SKD's UcsHandle.py file so it works with self-signed certs.  https://www.python.org/dev/peps/pep-0476/#opting-out.

```
# Workaround for Python 2.7.9 certificate validation (https://www.python.org/dev/peps/pep-0476/#opting-out)
import ssl
ssl._create_default_https_context = ssl._create_unverified_context
``