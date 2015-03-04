FROM vamship/zmq-baseline:1.0.0
MAINTAINER Vamshi K Ponnapalli <vamshi.ponnapalli@gmail.com>


# Nodejs configuration instructions from here:
# https://github.com/joyent/node/wiki/installing-node.js-via-package-manager#debian-and-ubuntu-based-linux-distributions
RUN curl -sL https://deb.nodesource.com/setup | bash -

# We need python 2.7 because some node modules require node-gyp,
# which in turn depends on python 2.7.
RUN apt-get install -y  nodejs\
                        python2.7

RUN npm config set python /usr/bin/python2.7
