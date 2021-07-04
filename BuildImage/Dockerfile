#FROM registry.access.redhat.com/ubi8/ubi
#FROM redhat/ubi8
FROM panubo/sshd

#FROM alpine

ENV SSH_ENABLE_ROOT=true
#ENV SSH_ENABLE_PASSWORD_AUTH=true 
#ENV SSH_ENABLE_ROOT_PASSWORD_AUTH=true

RUN apk update; apk add openrc python3
RUN openrc
RUN touch /run/openrc/softlevel

USER root
COPY containerkey.pub /root/.ssh/authorized_keys

# systemctl enable sshd 

#EXPOSE 22

#CMD [ "/sbin/init" ]
