GAE on Cloud9
=============

Using google app engine on CLoud9 currenlty requires you to compile or download
Python 2.7 and PIL in your workspace. You can then use the terminal to start,
stop and deploy google app engine applications.


Instalation
-----------

Install Python 2.7

```
wget http://www.python.org/ftp/python/2.7.3/Python-2.7.3.tgz
tar xvfz Python-2.7.3.tgz
cd Python-2.7.3 
./configure --prefix=$HOME
make
make install
cd ..
rm -rf Python-2.7.3*
```

Install App Engine

```
wget http://googleappengine.googlecode.com/files/google_appengine_1.7.2.zip
unzip google_appengine_1.7.2.zip
rm google_appengine_1.7.2.zip
mv google_appengine ../lib/
cd ../bin/
ln -s ../lib/google_appengine/*.py .
```

PIL
```
wget http://effbot.org/downloads/Imaging-1.1.7.tar.gz
tar xvfz Imaging-1.1.7.tar.gz
cd Imaging-1.1.7
python setup.py install
cd ..
rm -rf rm Imaging-1.1.7*
```

Run the app
-----------

```
dev_appserver.py -a $IP -p $PORT .
```