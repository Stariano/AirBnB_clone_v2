#!/usr/bin/python3
"""
Fabric script that generates a tgz archive from the contents of the web_static
folder of the AirBnB Clone repo
"""

from datetime import datetime
from fabric.api import local
from os.path import isdir


def do_pack():
	"""generates a tgz archive"""
	try:
		now = datetime.now()
		now = str(now).replace("-", "").replace(":","")
		now = now.replace(" ", "").replace(".", "")
		if isdir("versions") is False:
			local("mkdir versions")
		filee = "versions/web_static_{}.tgz".format(now)
		local("tar -cvzf {} web_static".format(filee))
		return filee
	except:
		return None
