#Install iojs on rasperry pi


* get bin archive from iojs.org
* extract the archve with tar -xf ...

* copy bin and lib to /usr/local/bin

			sudo cp -av iojs/bin/* /usr/local/bin
			sudo cp -av -r iojs/lib/node_modules /usr/local/lib/node_modules


