FROM ruby:2.7 AS base

WORKDIR /usr/src/app

RUN apt-get update \
  && apt-get install -y --no-install-recommends build-essential curl libpq-dev \
  && rm -rf /var/lib/apt/lists/* /usr/share/doc /usr/share/man \
  && apt-get clean \
  && useradd --create-home ruby \
  && chown ruby:ruby -R /usr/src/app \
  && chown ruby:ruby -R /usr/local/bundle

ENV RAILS_ENV="${RAILS_ENV:-development}" \
    PATH="${PATH}:/home/ruby/.local/bin" \
    PATH="${PATH}:/usr/local/bundle/bin" \
    USER="ruby"

USER ruby

RUN gem install rails:'< 7' bundler

CMD ["rails"]
