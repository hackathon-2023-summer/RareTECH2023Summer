-RareTECH2023Summer フォルダが親リポジトリ、backend フォルダ、frontend フォルダが子リポジトリになっている。

- 各リポジトリを Open Folder で開くことにより、Dev Container が使える。
- 親リポジトリの docker-compose.yml で Compose Up を実行すると nginx の向こう側に frontend と backend が展開される。
- その際、./frontend/public/index.html の window.API_BASE_URL を''にする。
- 動作不良で困ったら、./backend/alembic、./backend/alembic.ini、./backendmysql フォルダを削除する。 データベースは破壊されるので注意。
