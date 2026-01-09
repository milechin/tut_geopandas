FROM condaforge/miniforge3:latest

RUN apt-get update && apt-get install -y \
    unzip

# Copy environment.yml (if found) to a temp location so we update the environment. Also
# copy "noop.txt" so the COPY instruction does not fail if no environment.yml exists.
COPY environment.yml* .devcontainer/noop.txt /tmp/conda-tmp/
RUN if [ -f "/tmp/conda-tmp/environment.yml" ]; then umask 0002 && /opt/conda/bin/mamba env update -n base -f /tmp/conda-tmp/environment.yml; fi \
    && rm -rf /tmp/conda-tmp

USER ubuntu
EXPOSE 8888
RUN mkdir /home/ubuntu/notebooks
WORKDIR /home/ubuntu/notebooks
CMD ["/opt/conda/bin/jupyter", "notebook", "--NotebookApp.token=''", "--ip=0.0.0.0", "--no-browser"]

