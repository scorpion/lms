# Capture environment variables from passed arguments and setup default value.
ARG RABBITMQ_VER=${RABBITMQ_VER}
ARG RABBITMQ_IMAGE=${RABBITMQ_IMAGE}

# Image and version to pull
FROM ${RABBITMQ_IMAGE}:${RABBITMQ_VER}

# Ports to expose to host system
EXPOSE 4369 5671 5672 25672 15671 15672
