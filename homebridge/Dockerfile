FROM %%BASE_IMAGE%%

ENV LANG C.UTF-8

RUN apk add --no-cache jq python nodejs git make g++ avahi-compat-libdns_sd avahi-dev avahi-tools avahi-ui-tools
RUN npm config set unsafe-perm true
RUN npm install -g homebridge homebridge-homeassistant

COPY homebridge-base-config.json /etc/
COPY run.sh /
RUN chmod a+x /run.sh

EXPOSE 51826

CMD [ "/run.sh" ]
