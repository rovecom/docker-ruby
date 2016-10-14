FROM ruby:2.3.1
MAINTAINER Dennis de Vaal <ddevaal@rovecom.nl>

RUN mkdir -p /usr/src/app
WORKDIR /usr/src/app

RUN apt-get update && \
    apt-get install -y mysql-client nodejs --fix-missing --no-install-recommends
RUN gem install bundler --no-ri --no-rdoc

EXPOSE 3000

ONBUILD COPY Gemfile ./
ONBUILD COPY Gemfile.lock ./
ONBUILD RUN bundle install --no-deployment
ONBUILD COPY . /usr/src/app