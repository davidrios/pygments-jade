pygments-jade
=============

startup:

	$ virtualenv --no-site-packages pygenv
	$ source pygenv/bin/activate
	$ hg clone http://bitbucket.org/birkenfeld/pygments-main
	$ rm pygments-main/pygments/lexers/web.py
	$ ln code/web.py pygments-main/pygments/lexers/
	$ pushd pygments-main && python setup.py develop && popd
	$ deactivate

test:

	$ cd ../test
	$ ./generate