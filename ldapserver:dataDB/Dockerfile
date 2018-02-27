# @edt ASIX-m11 Curs 2017-2018
# ldapserver:dataDB
#servidor ldap creacio interactiu
#-----------------------------------------------------------------------
FROM fedora:24
MAINTAINER asixm11@edt "@edt ASIX-m11"
RUN dnf -y update vi
RUN dnf -y install vim procps iputils iproute tree nmap \
  openldap openldap-clients openldap-servers mlocate man-db \
  xinetd less
RUN mkdir /opt/docker/
COPY * /opt/docker/
COPY ldap.conf /etc/openldap/ 
RUN chmod +x /opt/docker/install.sh /opt/docker/startup.sh
RUN /opt/docker/install.sh

WORKDIR /opt/docker/ 
CMD ["/opt/docker/startup.sh"]
