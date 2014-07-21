##easyos
--------

A convenience-dictionary of common operating-system information needed while writing code.

#####Getting easyos:

Simply:

	pip install easyos

#####Using easyos is easy:

To list all the keys, simply import and print `easyos`:

	$ python
	>>> from easyos import easyos
	>>> from pprint import pprint
	>>> pprint(easyos)
	{'current_gid': 20,
	 'current_uid': 501,
	 'current_user': 'tfisher',
	 'current_user_desktop': '/Users/tfisher/Desktop',
	 'current_user_group': 'staff',
	 'current_user_homedir': '/Users/tfisher',
	 'current_user_plist_dir': '/Users/tfisher/./Library/LaunchAgents/',
	 'mount_dir': '/Volumes',
	 'os': 'Darwin',
	 'platform': 'Darwin-13.3.0-x86_64-i386-64bit',
	 'python_version': '2.7.8',
	 'release': '10.9.4',
	 'tmp_dir': '/var/folders/k6/dzxr5tss2kn_2tbbk_jfk4c40000gn/T',
	 'type': 'Darwin'}
	>>>
	
To use `easyos` in a script, simply call the relevant key:

	if easyos['os'] == 'Darwin' and easyos['python_version'] == '2.7.8': 
    	print "You're up to date!"


Abstract away the tedious bits of cross-platform coding:

	with open (easyos['tmp_dir']+'/script', 'w') as log:
	    message = "wow that's easy"
    	log.write(message)
    	
    	


######New features / Pull requests:

Make a pull request with your change or addition and I'll merge it if nudges the module in the right direction.

As a non-Windows user, I'm unlikely to add more Windows attributes, but if you need something added, simply branch, make a pull request, and I'll likely merge.