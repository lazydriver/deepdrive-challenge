FROM deepdriveio/deepdrive
#FROM python:3

#COPY requirements.txt /requirements.txt

#RUN apt-get update && apt-get install -y libjemalloc-dev libboost-dev \
#                                         libboost-filesystem-dev \
#                                         libboost-system-dev \
#                                         libboost-regex-dev \
#                                         python3-dev \
#                                         autoconf \
#                                         flex \
#                                         bison

#RUN git clone https://github.com/deepdrive/deepdrive-api.git && \
#    pip install --upgrade pip && \
#    pip install --use-pep517 ./deepdrive-api

COPY ./agent.py /

WORKDIR /

COPY ./entrypoint.bash /

ENTRYPOINT ["/entrypoint.bash"]
CMD ["python","/agent.py"]
