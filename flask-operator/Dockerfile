# Build the manager binary
FROM quay.io/operator-framework/helm-operator:v1.1.0

LABEL name="Flask Operator" \
      vendor="IBM Edge" \
      version="v0.0.1" \
      release="1" \
      summary="This is an example of a flask helm operator." \
      description="This operator will deploy flask application to the cluster."

# Required Licenses
COPY licenses /licenses

ENV HOME=/opt/helm
COPY watches.yaml ${HOME}/watches.yaml
COPY helm-charts  ${HOME}/helm-charts
WORKDIR ${HOME}
