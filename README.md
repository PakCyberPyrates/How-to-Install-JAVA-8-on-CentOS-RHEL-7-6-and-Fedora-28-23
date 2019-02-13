Step 1 – Download Latest Java Archive

cd /opt/

wget --no-cookies --no-check-certificate --header "Cookie: gpw_e24=http%3A%2F%2Fwww.oracle.com%2F; oraclelicense=accept-securebackup-cookie" "https://download.oracle.com/otn-pub/java/jdk/8u201-b09/42970487e3af4f5aa5bca3f542482c60/jdk-8u201-linux-x64.tar.gz"

tar xzf jdk-8u201-linux-x64.tar.gz

Step 2 – Install Java 8 with Alternatives

cd jdk1.8.0_201/

alternatives --install /usr/bin/java java /opt/jdk1.8.0_201/bin/java 2

alternatives --config java


alternatives --install /usr/bin/jar jar /opt/jdk1.8.0_201/bin/jar 2


alternatives --install /usr/bin/javac javac /opt/jdk1.8.0_201/bin/javac 2

alternatives --set jar /opt/jdk1.8.0_201/bin/jar

alternatives --set javac /opt/jdk1.8.0_201/bin/javac

Step 3 – Check Installed Java Version

java -version

Step 4 – Setup Java Environment Variables

export JAVA_HOME=/opt/jdk1.8.0_201


export JRE_HOME=/opt/jdk1.8.0_201/jre


export PATH=$PATH:/opt/jdk1.8.0_201/bin:/opt/jdk1.8.0_201/jre/bin

Also add the above commands to /etc/bashrc or /etc/environment file to auto set environment variables during the system reboot.
