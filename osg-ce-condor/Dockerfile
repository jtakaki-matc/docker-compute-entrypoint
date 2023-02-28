FROM base AS osg-ce-condor
ARG BASE_YUM_REPO=release
LABEL maintainer "OSG Software <help@opensciencegrid.org>"
LABEL name "osg-ce-condor"

RUN yum install -y osg-ce-condor && \
    yum clean all && \
    rm -rf /var/cache/yum/

COPY osg-ce-condor/etc/osg/image-config.d/* /etc/osg/image-config.d/
COPY osg-ce-condor/etc/condor/config.d/* /etc/condor/config.d/
COPY osg-ce-condor/usr/local/bin/* /usr/local/bin/
COPY osg-ce-condor/etc/supervisord.d/* /etc/supervisord.d/