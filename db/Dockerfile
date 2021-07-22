FROM mysql:8.0
LABEL maintainer="y-okamoto-1113 <okamoto.yuuki.1113+github@gmail.com>"

ENV TZ=Asia/Tokyo

COPY ./db/my.cnf /etc/my.cnf

# TODO: MySQLのエラーログ設定がうまくいかない
# RUN mkdir -p /var/log/mysql && touch /var/log/mysql/mysql-error.log
# RUN chown mysql:mysql /var/log/mysql
# RUN rm -rf /var/lib/mysql/*
