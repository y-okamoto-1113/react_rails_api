FROM nginx:stable
LABEL maintainer="y-okamoto-1113 <okamoto.yuuki.1113+github@gmail.com>"
ENV TZ=Asia/Tokyo

# インクルード用のディレクトリ内を削除
RUN rm -f /etc/nginx/conf.d/*

# Nginxの設定ファイルをコンテナにコピー
COPY ./web/nginx.conf /etc/nginx/conf.d/

# ビルド完了後にNginxを起動
CMD /usr/sbin/nginx -g 'daemon off;' -c /etc/nginx/nginx.conf
