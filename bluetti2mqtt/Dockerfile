ARG BUILD_FROM
FROM $BUILD_FROM

# Copy data for add-on
COPY rootfs /

# Install bluetti_mqtt
RUN apk add --update --no-cache bluez git
RUN pip install git+https://github.com/boy-wonder/bluetti_mqtt --requirement requirements.txt
run apk del git \
	&& rm -rf /var/cache/apk/* /lib/apk/db/*

CMD [ "/run.sh" ]
