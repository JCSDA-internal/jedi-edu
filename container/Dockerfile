FROM jcsda/docker-clang-mpich-dev:latest
RUN pip install jupyter -U && pip install jupyterlab
RUN pip install bash_kernel && python -m bash_kernel.install

COPY start /srv
RUN chmod +x /srv/start

EXPOSE 8888
USER jedi
WORKDIR /home/jedi
ENV SHELL /bin/bash
ENTRYPOINT ["/srv/start"]
#ENTRYPOINT ["jupyter", "lab","--ip=0.0.0.0","--allow-root"]
