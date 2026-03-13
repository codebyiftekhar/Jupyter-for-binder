FROM ubuntu:22.04

RUN apt-get update && \
    apt-get install -y \
    build-essential \
    wget \
    curl \
    git \
    ca-certificates \
    cmake \
    python3 python3-pip && \
    apt-get clean

RUN pip3 install notebook jupyterlab
RUN apt-get install -y clang libclang-dev && \
    conda install -c conda-forge xeus-cling=0.17.2 cling=0.11.1 notebook -y

WORKDIR /home/jovyan

CMD ["jupyter", "notebook", "--ip=0.0.0.0", "--port=8888", "--no-browser", "--allow-root"]
