cron ジョブに登録してシェルを実行する
#####################################

通常シェルは、ニュースレターを送ったり、たまにデータベースをクリーンアップしたりすることを、
cron ジョブとして実行します。

このように簡単な設定で行えます。::

      */5  *    *    *    *  cd /full/path/to/app && bin/cake myshell myparam
    # *    *    *    *    *  実行するコマンド
    # │    │    │    │    │
    # │    │    │    │    │
    # │    │    │    │    \───── 曜日 (0 - 6) (0 から 6 が日曜日から土曜日、
    # |    |    |    |           もしくは曜日名)
    # │    │    │    \────────── 月 (1 - 12)
    # │    │    \─────────────── 日 (1 - 31)
    # │    \──────────────────── 時 (0 - 23)
    # \───────────────────────── 分 (0 - 59)

詳しくはこちら: http://ja.wikipedia.org/wiki/Crontab

.. meta::
    :title lang=ja: cron ジョブに登録してシェルを実行する
    :keywords lang=ja: cron ジョブ,bash script,crontab
