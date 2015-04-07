FROM apsl/circusbase
MAINTAINER APSL <bcabezas@apsl.net>

# install java jdk oracle 1.5.0-22 from script. 
# https://ivan-site.com/2012/05/download-oracle-java-jre-jdk-using-a-script/
RUN \
    cd /tmp ;\
    /usr/bin/wget --no-cookies --no-check-certificate \
        --header "Cookie: gpw_e24=http%3A%2F%2Fwww.oracle.com%2F; oraclelicense=accept-securebackup-cookie"  \
        http://download.oracle.com/otn-pub/java/jdk/1.5.0_22/jdk-1_5_0_22-linux-amd64.bin

# alternate  java method disabled: download local jdk
#ADD jdk-1_5_0_22-linux-amd64.bin /tmp/

# install java
RUN \
    echo yes|sh /tmp/jdk-1_5_0_22-linux-amd64.bin ;\
    rm /tmp/jdk-1_5_0_22-linux-amd64.bin

ENV JAVA_HOME /jdk1.5.0_22
ENV PATH /jdk1.5.0_22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
