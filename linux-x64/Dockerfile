FROM 100.125.0.31:20202/zhoujiawei/cross-compiler:base.1

ENV CROSS_TRIPLE x86_64-linux-gnu
ENV CROSS_ROOT /usr/${CROSS_TRIPLE}
ENV PATH ${PATH}:${CROSS_ROOT}/bin
ENV LD_LIBRARY_PATH ${CROSS_ROOT}/lib:${LD_LIBRARY_PATH}
ENV PKG_CONFIG_PATH ${CROSS_ROOT}/lib/pkgconfig:${PKG_CONFIG_PATH}

RUN mkdir -p ${CROSS_ROOT} && \
    cd /usr/bin && \
    ln -s ${CROSS_TRIPLE}-gcc ${CROSS_TRIPLE}-cc && \
    ln -s ${CROSS_TRIPLE}-g++ ${CROSS_TRIPLE}-c++
