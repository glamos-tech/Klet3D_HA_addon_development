ARG BUILD_FROM
FROM $BUILD_FROM

RUN \
  apk --no-cache add \
  nginx \
  \
  && mkdir -p /run/nginx

COPY ingress.conf /etc/nginx/http.d/
COPY . /build
COPY run.sh /
RUN chmod a+x /run.sh

CMD /run.sh