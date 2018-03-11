from ubuntu:bionic
ENV GO_INSTALL_FILE go1.10.linux-amd64.tar.gz
RUN apt-get update && \
apt-get install -y build-essential git vim wget tmux zsh
RUN wget https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh -O - | zsh || true
RUN cd /tmp && \
    wget https://dl.google.com/go/${GO_INSTALL_FILE} && \
    tar -xf ${GO_INSTALL_FILE} && \
    mv go /opt && \
    ln -s /opt/go/bin/* /usr/bin/
WORKDIR /workspace
CMD ["/bin/zsh"]
