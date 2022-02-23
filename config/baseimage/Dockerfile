#
# Copyright Greg Haskins All Rights Reserved.
#
# SPDX-License-Identifier: Apache-2.0
#
FROM --platform=arm64 eclipse-temurin:8-jre
COPY scripts /tmp/scripts
RUN cd /tmp/scripts && \
    common/packages.sh && \
    common/setup.sh && \
    docker/fixup.sh && \
    common/cleanup.sh && \
    rm -rf /tmp/scripts
ENV GOPATH=/opt/gopath
ENV GOROOT=/opt/go
ENV PATH=$PATH:$GOROOT/bin:$GOPATH/bin
