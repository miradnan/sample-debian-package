# Sample debian package

These are the default files that you'll need to build your deb package on.
Compile your source code and place it under `/usr/sbin/package-name` file

### Building Debian package
```bash
sudo apt-get update
sudo apt install -y software-properties-common wget ruby-full git devscripts build-essential lintian
sudo dpkg-deb --build package-name
```

# Test your package
```bash
sudo dpkg -i package-name.deb
# see if its running
ps aux | grep package-name
/etc/init.d/package-name status
```
