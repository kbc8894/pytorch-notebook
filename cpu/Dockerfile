# Copyright (c) Jupyter Development Team.
# Distributed under the terms of the Modified BSD License.
ARG BASE_CONTAINER=jupyter/scipy-notebook
FROM $BASE_CONTAINER

LABEL maintainer="ByungchanKim <kbc8894@gmail.com>"

# Install Pytorch
RUN pip install --quiet --no-cache-dir \
    torch==1.7.1+cpu \
    torchvision==0.8.2+cpu \
    torchaudio==0.7.2 \
    -f https://download.pytorch.org/whl/torch_stable.html && \
    fix-permissions "${CONDA_DIR}" && \
    fix-permissions "/home/${NB_USER}"
