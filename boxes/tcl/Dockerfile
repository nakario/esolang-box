FROM esolang/build-base

RUN apk add --update tcl expect && \
    mkdir /tmp/tcllib && \
    (curl -L https://github.com/tcltk/tcllib/archive/tcllib_1_18.tar.gz | tar -xz -C /tmp/tcllib --strip-components=1) && \
    tclsh /tmp/tcllib/installer.tcl -no-html -no-nroff -no-examples -no-gui -no-apps -no-wait -pkg-path /usr/lib/tcllib && \
    rm -rf /var/cache/apk/* /tmp/tcllib && \
    ln -s /bin/script /bin/tcl

COPY script /root/script

