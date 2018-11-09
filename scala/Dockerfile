FROM openjdk:8u151-jdk

# ENV SCALA_VERSION=2.12.6

# RUN apt-get update \
#  && wget https://downloads.lightbend.com/scala/${SCALA_VERSION}/scala-${SCALA_VERSION}.deb \
#  && dpkg -i scala-${SCALA_VERSION}.deb \
#  && rm -f scala-${SCALA_VERSION}.deb \
#  && apt-get autoremove \
#  && apt-get autocleanFROM


ENV SBT_VERSION=1.2.6

RUN apt-get update \
 && curl -sL https://github.com/sbt/sbt/releases/download/v${SBT_VERSION}/sbt-${SBT_VERSION}.tgz | tar xzf - -C /usr/local \
 && ln -s /usr/local/sbt/bin/sbt /usr/local/bin/sbt \
 && sbt exit \
 && apt-get autoremove \
 && apt-get autoclean

WORKDIR /usr/local

CMD ["/bin/bash"]