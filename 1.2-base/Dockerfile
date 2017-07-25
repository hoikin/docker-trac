FROM centos

RUN yum -y install epel-release wget python-pip

RUN pip install --upgrade pip

RUN pip install Genshi

RUN easy_install Trac

RUN trac-admin /root/trac-project initenv

RUN yum -t install subversion subversion-python

RUN tracd --port 80 /root/trac-project
