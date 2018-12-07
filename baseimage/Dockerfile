FROM continuumio/miniconda3:4.5.11

COPY environment.yml environment.yml
RUN conda config --add channels conda-forge \
    && conda env create -f environment.yml \
    && rm -rf /opt/conda/pkgs/*

ENTRYPOINT [ "/bin/bash", "ls" ]

