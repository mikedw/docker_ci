FROM circleci/android:api-29

USER root

# Install ruby
RUN apt-get update && \
    apt-get install -y ruby-dev

# Install fastlane
RUN gem install fastlane \
    && gem install bundler \
    && rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* \
    && apt-get autoremove -y && apt-get clean

# Install Firebase CLI
RUN curl -sL firebase.tools | bash

USER circleci
