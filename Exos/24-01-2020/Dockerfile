FROM ubuntu
RUN apt-get update
RUN apt-get install -qy python3 python3-pip git virtualenv
RUN mkdir ./app && cd ./app
RUN git config --global user.name MyUsername && git config --global user.email MyEmail@gmail.com && git clone https://github.com/ohsr/bigDataCourse
COPY . /app
WORKDIR ./app
EXPOSE 8888
RUN pip3 install -r Requirements
CMD ["jupyter","notebook","--ip=0.0.0.0","--port=8888","--allow-root"]