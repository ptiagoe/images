FROM continuumio/miniconda3:4.5.11

RUN conda create -n env python=3.6
COPY environment.yml environment.yml

RUN conda config --add channels conda-forge \
    && conda env create --force -n env -f environment.yml \
    && rm -rf /opt/conda/pkgs/*

RUN echo "source activate env" > ~/.bashrc
ENV PATH /opt/conda/envs/env/bin:$PATH

ENTRYPOINT [ "/bin/bash","cat" ]

