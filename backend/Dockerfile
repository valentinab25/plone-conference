ARG PLONE_VERSION=6.0.0b3
FROM plone/plone-backend:${PLONE_VERSION}

LABEL maintainer="valentina <valentina.balan@eaudeweb.ro>" \
      org.label-schema.name="plone-conference-backend" \
      org.label-schema.description="Plone Conference backend image." \
      org.label-schema.vendor="valentina"

# Add local code
COPY . .

# Install local requirements and fix permissions
RUN ./bin/pip install -r requirements.txt \
    && chown -R plone: /app
