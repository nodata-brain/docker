# ベースイメージの設定
FROM php:7.2-apache

# 作業ディレクトリ
WORKDIR {workdir}

# 設定ファイル
ENV PATH $PATH:/var/www/html/config
RUN echo 'alias ll="ls -la"' >> ~/.bashrc
RUN apt-get update
RUN apt-get -y install vim
RUN apt-get -y install mysql-server

ADD {copyfile} /var/www/
COPY ./php.ini /usr/local/etc/php/
