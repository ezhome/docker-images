FROM circleci/golang:1.10

RUN sudo apt-get update && sudo apt-get install -y --no-install-recommends python-pip python-setuptools
RUN sudo pip install awscli
RUN wget https://releases.hashicorp.com/terraform/0.11.3/terraform_0.11.3_linux_amd64.zip \
    && sudo unzip terraform_0.11.3_linux_amd64.zip -d /usr/bin/

RUN mkdir -p ~/go
RUN echo 'export PATH=/home/circleci/go/bin:$PATH' >> /home/circleci/.bashrc
ENV GOPATH=/home/circleci/go
