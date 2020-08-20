# 在docker建立redis

## Step
1. 安裝 docker, docker-compose
2. 將`docker-compose.yml.default` 檔名改成 `docker-compose.yml`
3. 編輯 `docker-compose.yml`，選擇image(redis映像檔以及版本)，定義`port`,`password`
4. 創建：開啟命令列執行 `docker-compose up -d`
 - 執行 `docker ps` 看看有沒有開啟成功，這裡可以看到container id
 -  執行 `docker exec -it <container_id | container_name> /bin/bash` 即可進入該container的bash
 - 進入bash後，執行`redis-cli -a '<密碼>'`即可進入redis
5. 測試：將`testCon.js.default`改成`testCon.js`，
並執行`node testCon.js`，看看是否顯示**con ready**（請先`npm install`或`yarn`）

### 參考（ref): https://zhuanlan.zhihu.com/p/43654441