FROM ctng

RUN useradd -m myuser
USER myuser
ENV HOME=/home/myuser
WORKDIR $HOME
ADD .config $HOME/.config
RUN ct-ng build
