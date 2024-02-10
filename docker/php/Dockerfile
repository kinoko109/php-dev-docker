FROM php:8.1.18-fpm

# ローカルのphp.iniファイルをコンテナにコピー
COPY php.ini /usr/local/etc/php/

# パッケージ諸々インストール
RUN apt-get update && apt-get install -y \
	git \
	curl \
	zip \
	unzip \
    && docker-php-ext-install pdo_mysql

# 作業ディレクトリを/var/wwwに設定
# WORKDIR を指定すると、それ以降、コンテナ内のすべてのコマンド（ Dockerfile 内の CMD や COPY など）は、指定されたディレクトリ（この場合は /var/www ）で実行される。
WORKDIR /var/www