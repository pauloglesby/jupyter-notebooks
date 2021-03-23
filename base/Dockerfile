ARG JUPYTER_BASE=jupyter/minimal-notebook:9fe5186aba96

FROM ${JUPYTER_BASE}

LABEL maintainer="Paul Aliabadi-Oglesby <paul.oglesby@gmail.com>"

COPY --chown=${NB_UID}:${NB_GID} requirements.txt /tmp/

RUN pip install --requirement /tmp/requirements.txt && \
    fix-permissions $CONDA_DIR && \
    fix-permissions /home/$NB_USER
