FROM nginx:stable

# インクルード用の conf を削除
RUN rm /etc/nginx/conf.d/default.conf

# Nginx の設定ファイルをコンテナにコピー
ADD ./docker/nginx/nginx.conf /etc/nginx/conf.d/ecs-rails-sample.conf

# ビルド完了後に Nginx を起動
CMD /usr/sbin/nginx -g 'daemon off;' -c /etc/nginx/nginx.conf
