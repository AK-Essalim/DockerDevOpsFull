FROM ruby:2.6.0-alpine
WORKDIR /app
RUN apk add --update nodejs ruby-nokogiri ruby-dev build-base tzdata sqlite-dev

COPY rails-example-project .
RUN gem install bundler
RUN bundle install
RUN rails db:migrate

EXPOSE 3000
CMD ["rails", "s"]