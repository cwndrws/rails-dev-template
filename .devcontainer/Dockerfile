FROM ruby:3

# setup yarn source
RUN curl -sS https://dl.yarnpkg.com/debian/pubkey.gpg | apt-key add -
RUN echo "deb https://dl.yarnpkg.com/debian/ stable main" | tee /etc/apt/sources.list.d/yarn.list

# update system deps
RUN apt update -y
RUN apt upgrade -y

# install yarn
RUN apt install -y yarn

# setup user
RUN useradd -ms /bin/bash user && \
    adduser user sudo
USER user
WORKDIR /home/user

# update gems
RUN gem update

# install rails
RUN gem install rails
