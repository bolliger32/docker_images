ARG TRAVIS_COMMIT=${TRAVIS_COMMIT}
FROM rhodium/worker:${TRAVIS_COMMIT}
ARG DEBIAN_FRONTEND=noninteractive

## filepath curation
COPY octave_environment.yml /opt/conda/specs/octave_environment.yml

## install octave
RUN sudo apt-get update && sudo apt-get install -yq octave

# add octave-specific packages
RUN conda env update -f /opt/conda/specs/octave_environment.yml
