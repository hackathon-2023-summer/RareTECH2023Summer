-RareTECH2023Summer フォルダが親リポジトリ、backend フォルダ、frontend フォルダが子リポジトリになっている。

- 各リポジトリを Open Folder で開くことにより、Dev Container が使える。
- 親リポジトリの docker-compose.yml で Compose Up を実行すると nginx の向こう側に frontend と backend が展開される。
- その際、./frontend/public/index.html の window.API_BASE_URL を''にする。
- 動作不良で困ったら、./backend/alembic、./backend/alembic.ini、./backendmysql フォルダを削除する。 データベースは破壊されるので注意。

- 任意のフォルダで
  　 git clone --recurse-submodules https://github.com/hackathon-2023-summer/RareTECH2023Summer  
  これを実行すると、親子関係のリポジトリができる。

- ./.env、./backend/.env、./frontend/.env の 3 つの.env を移植すること。

- AWS 用のコンテナ起動コマンドは以下。MySQL を止めている。
  docker compose -f "docker-compose-aws.yml" up -d --build
