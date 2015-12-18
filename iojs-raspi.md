# Install iojs on rasperry pi

* get bin archive from iojs.org
* extract the archve with tar -xf ...

* copy bin and lib to /usr/local/bin

			sudo cp -av iojs/bin/* /usr/local/bin
			sudo cp -av -r iojs/lib/node_modules /usr/local/lib/node_modules


# Alternative

Instead of copying the files, simply move the whole folder to e.g. /opt/ and add the folder to the path

	echo "export PATH=$PATH:/opt/node-v0.12.3-linux-x64/bin" > /etc/profile.d/node-npm.sh
	


	# Create a softlink to node in /usr/bin/
	ln -s /opt/node-v*-linux-x64/bin/node /usr/bin/node
	# Create a softlink to npm  in /usr/bin/
	ln -s /opt/node-v*-linux-x64/bin/npm  /usr/bin/npm
	# Create a softlink to iojs in /usr/bin (this step can be omitted if you're using node)
	ln -s /opt/node-v*-linux-x64/bin/iojs /usr/bin/iojs
	
	
