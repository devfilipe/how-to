
# Eclipse

**Table of Contents**

[TOCM]

[TOC]

## How to Install the Latest Eclipse IDE on Ubuntu 18.04?

At the time of writing this article, the latest stable version of Eclipse is 
Eclipse 2019-03 (4.11.0).

To install Eclipse on your Ubuntu system, follow these steps:

**1. Install Java.**

Eclipse is a Java-based application and it requires a Java runtime environment (JRE)
to be installed in order to run. Install the default OpenJDK package with:
```bash
sudo apt install default-jre
```

**2. Install Eclipse.**

We will be installing Eclipse using the snappy packaging system. To download and 
install the Eclipse snap package on your system, type:
```bash
sudo snap install --classic eclipse
```

On successful installation of Eclipse, you should see the following output:
```
eclipse 2019-03 from Snapcrafters installed
```

3. Reference
[Linuxize](https://linuxize.com/post/how-to-install-the-latest-eclipse-ide-on-ubuntu-18-04/)
