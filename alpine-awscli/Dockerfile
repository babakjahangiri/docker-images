# Use Alpine Linux as the base image
FROM alpine:latest

MAINTAINER babakjahan

# Update and install dependencies
RUN apk add --no-cache \
    groff \
    less \
    zip \
    curl


# curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip"
# Install AWS CLI v2 (replacing `pip` with `curl` and `unzip`)
RUN curl "https://s3.amazonaws.com/aws-cli/awscli-bundle.zip" -o "awscli-bundle.zip"\
    && unzip awscli-bundle.zip \
    && ./aws/install \
    && rm -rf awscli-bundle.zip ./aws

# Verify the installation
RUN aws --version

# Set up a working directory
WORKDIR /data

# Set the default command for the container
CMD ["/bin/sh"]