FROM erwinsteffens/ruby:2.3.1
MAINTAINER Dennis de Vaal <ddevaal@rovecom.nl>

ONBUILD COPY Gemfile ./
ONBUILD COPY Gemfile.lock ./
ONBUILD RUN bundle install --no-deployment
ONBUILD COPY . /usr/src/app