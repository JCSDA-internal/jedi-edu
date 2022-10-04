FROM jcsda/docker-clang-mpich-dev:edu
RUN pip3 install jupyter -U && pip3 install jupyterlab
RUN pip3 install bash_kernel && python3 -m bash_kernel.install

COPY start /srv
RUN chmod +x /srv/start

EXPOSE 8888
USER nonroot
WORKDIR /home/nonroot
ENV SHELL /bin/bash
ENTRYPOINT ["/srv/start"]
#ENTRYPOINT ["jupyter", "lab","--ip=0.0.0.0","--allow-root"]
