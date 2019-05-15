FROM golang:1.12

RUN apt-get update && \
    DEBIAN_FRONTEND=noninteractive apt-get install -y vim && \
    apt-get clean

RUN DEBIAN_FRONTEND=noninteractive apt-get install -y vim-nox && \
    apt-get clean

RUN apt-get install -y ctags && apt-get clean

# VIM plugin for go
RUN git clone https://github.com/VundleVim/Vundle.vim.git ~/.vim/bundle/Vundle.vim


COPY vimrc /root/.vimrc
RUN cd /go
RUN echo -ne '\n' |vim +PluginInstall +qall
RUN echo -ne '\n' |vim  +GoInstallBinaries +qall; exit 0
RUN go get -u github.com/kardianos/govendor
