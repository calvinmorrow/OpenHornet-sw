FROM ubuntu:22.04

RUN useradd -ms /bin/bash openhornet

# Install dependencies
RUN apt-get -y update \
 && apt-get -y install \
    arduino \
    arduino-mk \
    bsdmainutils \
    curl \
 && rm -rf /var/lib/apt/lists/*

RUN curl -L https://api.github.com/repos/sparkfun/Arduino_Boards/tarball/main | tar xz --strip-components=1 -C /usr/share/arduino/hardware

ENV ARDUINO_DIR /usr/share/arduino
ENV ARDMK_DIR /usr/share/arduino
ENV PROMICRO_DIR /usr/share/arduino/hardware/sparkfun

USER openhornet
WORKDIR /home/openhornet

CMD ["/bin/bash", "-c", "make"]
