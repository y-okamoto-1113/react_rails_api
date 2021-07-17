FROM ruby:3.0.2
ENV BUILD_PACKAGES="bash" \
    RAILS_ENV="development"

RUN curl -sS https://dl.yarnpkg.com/debian/pubkey.gpg | apt-key add - \
    && echo "deb https://dl.yarnpkg.com/debian/ stable main" | tee /etc/apt/sources.list.d/yarn.list \
    && apt-get update -qq \
    && apt-get install -y $BUILD_PACKAGES
WORKDIR /myapp
COPY Gemfile /myapp/Gemfile
COPY Gemfile.lock /myapp/Gemfile.lock
RUN bundle install
RUN rails action_text:install
COPY . /myapp

EXPOSE 3000
