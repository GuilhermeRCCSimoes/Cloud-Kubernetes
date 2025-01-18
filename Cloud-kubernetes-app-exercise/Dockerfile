FROM odoo:18

USER root

COPY ./configs/odoo.conf /etc/odoo/odoo.conf

ENV ODOO_RC /etc/odoo/odoo.conf

VOLUME ["/var/lib/odoo"]

USER odoo

EXPOSE 8069 8072

CMD [ "odoo", "-c","/etc/odoo/odoo.conf" ]
