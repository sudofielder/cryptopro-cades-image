# cryptopro-cades-image
docker file 4 work with cryptopro extension (cades browser plug-in) *browser chrome*

use build.sh from building directory
#!/bin/bash

CSP_VERSION="4.0"
HTTP_PROXY="***"
HTTPS_PROXY="***"
IMAGE_TIMEZONE="***"

# Example build line
# --build-arg IMAGE_TIMEZONE="Europe/Moscow"
docker build --force-rm -f /tmp/chrome_csp/Dockerfile  --build-arg image_timezone=${IMAGE_TIMEZON} --build-arg http_proxy=${HTTP_PROXY} --build-arg https_proxy=${HTTPS_PROXY} --build-arg CSP_VERSION=${CSP_VERSION} -t "selenoid/chrome_csp:${CSP_VERSION}" .
