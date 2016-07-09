# rpmbuild-phantomjs

Create a phantomjs RPM for RHEL/CentOS.

## Requirements

To download package sources and install build dependencies

    yum -y install rpmdevtools yum-utils

## Build process

To build the package follow the steps outlined below

    git clone https://github.com/linuxhq/rpmbuild-phantomjs.git rpmbuild
    mkdir rpmbuild/SOURCES
    spectool -g -R rpmbuild/SPECS/phantomjs.spec
    yum-builddep rpmbuild/SPECS/phantomjs.spec
    rpmbuild -ba rpmbuild/SPECS/phantomjs.spec

## License

BSD

## Author Information

This package was created by [Taylor Kimball](http://www.linuxhq.org).
