FROM python:3.8

ENV PIP_DISABLE_PIP_VERSION_CHECK 1
ENV PYTHONBUFFERED 1
ENV PYTHONDONTWRITEBYTECODE 1

RUN mkdir /src

COPY . /src/

WORKDIR /src

RUN pip install --trusted-host=pypi.org --trusted-host=files.pythonhosted.org --upgrade pip
RUN pip install --trusted-host=pypi.org --trusted-host=files.pythonhosted.org --no-cache-dir -r requirements.txt
RUN chmod +x ./docker-entrypoint.sh

ENTRYPOINT ["./docker-entrypoint.sh"]