FROM python:2

ENV trac_version=87725e58ed4b75b7c4f53a7b6d96f79094f8f08f

# https://trac.edgewall.org/browser/trunk/INSTALL.rst
RUN easy_install \
  Genshi \
  pytz \
  Babel \
  docutils \
  Pygments \
  MySQL-python==1.2.5

RUN cd /usr/src && \
  curl -sL https://codeload.github.com/edgewall/trac/tar.gz/$trac_version | tar xvz && \
  cd trac-$trac_version/ && \
  python ./setup.py install && \
  cd .. && \
  rm -Rf trac-$trac_version/
