FROM gcr.io/google_appengine/python

# Create a virtualenv for the application dependencies.
# If you want to use Python 3, add the -p python3.4 flag.
RUN virtualenv /env
ENV VIRTUAL_ENV /env
ENV PATH /env/bin:$PATH

# Install dependencies.
ADD requirements.txt /app/requirements.txt
RUN pip install -r /app/requirements.txt

# Uncomment the following line to use NODB
# DEVELOP will use SQLite and in-memory cache insstead of Postgres And Redis
# This is useful to test the rest of the Django setup without configuring the database/cache
# Comment it out and rebuild this image once you have Postgres and Redis services in your cluster
#ENV DEVELOP 1

# Add application code.
ADD . /app

CMD export DJANGO_PASSWORD=$(cat /etc/secrets/djangouserpw); gunicorn -b :$PORT brounder.wsgi
