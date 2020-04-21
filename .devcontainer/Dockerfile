FROM ruby:2

# setup yarn source
RUN curl -sS https://dl.yarnpkg.com/debian/pubkey.gpg | apt-key add -
RUN echo "deb https://dl.yarnpkg.com/debian/ stable main" | tee /etc/apt/sources.list.d/yarn.list

# update system deps
RUN apt update -y
RUN apt upgrade -y

# update gems
RUN gem update

# install rails
RUN gem install rails

# install yarn
RUN apt install -y yarn