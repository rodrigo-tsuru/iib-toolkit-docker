FROM rodrigotsuru/ibmim-docker
MAINTAINER Rodrigo Tsuru <caixapostal@gmail.com>
RUN yum install -y curl \
tar \
glibc.i686 \
libgcc.i686
RUN cd /tmp && curl -O -L https://googledrive.com/host/0B1TfHhOuw5TLMWw2YkNITVhWWjQ/9.0.0-IIB-LINUXX64-DEVELOPER-TOOLKIT.tar.gz
RUN cd /tmp && \
tar -zvxf 9.0.0-IIB-LINUXX64-DEVELOPER-TOOLKIT.tar.gz && \
rm 9.0.0-IIB-LINUXX64-DEVELOPER-TOOLKIT.tar.gz
COPY install.xml /tmp/install.xml
RUN cd /tmp/Integration_Toolkit/ && \
/opt/IBM/InstallationManager/eclipse/tools/imcl input /tmp/install.xml -acceptLicense -showProgress  && \
rm -Rf /tmp/Integration_Toolkit