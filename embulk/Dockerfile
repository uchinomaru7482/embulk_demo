FROM openjdk:8

# embulkインストール
RUN curl --create-dirs -o /usr/local/bin/embulk -L "https://dl.embulk.org/embulk-latest.jar" &&\
    chmod +x /usr/local/bin/embulk

# 各種プラグインインストール
RUN embulk gem install embulk-input-mysql
RUN embulk gem install embulk-output-mysql
RUN embulk gem install embulk-filter-concat
RUN embulk gem install embulk-filter-column

# digdagインストール
RUN curl -o /usr/local/bin/digdag --create-dirs -L "https://dl.digdag.io/digdag-latest" &&\
    chmod +x /usr/local/bin/digdag
