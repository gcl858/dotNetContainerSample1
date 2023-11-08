
# dotNetContainerSample1
.Net應用容器化範例1

## 使用免費的 play with docker
https://labs.play-with-docker.com/

## 新增一個新的 instance

## 下載 Docker Compose的 yaml 檔

複製下面指令並到PWD的terminal上按[shift]+[insert]貼上後執行

    curl -LJO https://raw.githubusercontent.com/gcl858/dotNetContainerSample1/main/docker-compose.yml
結果畫面：![enter image description here](https://raw.githubusercontent.com/gcl858/dotNetContainerSample1/main/images/%E8%9E%A2%E5%B9%95%E5%BF%AB%E7%85%A7%202023-11-08%2009-44-02.png)

## 開始佈署
執行以下命令：

    docker compose -f docker-compose.yml up -d
結果畫面：
![enter image description here](https://raw.githubusercontent.com/gcl858/dotNetContainerSample1/main/images/%E8%9E%A2%E5%B9%95%E5%BF%AB%E7%85%A7%202023-11-08%2010-05-44.png)

## 透過"Open Port" 連結開啟網頁

點選8080 port

![enter image description here](https://raw.githubusercontent.com/gcl858/dotNetContainerSample1/main/images/%E8%9E%A2%E5%B9%95%E5%BF%AB%E7%85%A7%202023-11-08%2010-09-38.png)

![enter image description here](https://raw.githubusercontent.com/gcl858/dotNetContainerSample1/main/images/%E8%9E%A2%E5%B9%95%E5%BF%AB%E7%85%A7%202023-11-08%2010-15-26.png)

## 網址後加入/ims/並瀏覽
正常可以看到模擬共用auth畫面，可編輯json內容
![enter image description here](https://raw.githubusercontent.com/gcl858/dotNetContainerSample1/main/images/%E8%9E%A2%E5%B9%95%E5%BF%AB%E7%85%A7%202023-11-08%2010-17-36.png)

## 點擊"MyWeb1"瀏覽Blazor wasm應用
![enter image description here](https://raw.githubusercontent.com/gcl858/dotNetContainerSample1/main/images/%E8%9E%A2%E5%B9%95%E5%BF%AB%E7%85%A7%202023-11-08%2010-23-22.png)

目前透過網址後加參數資料，使openresty寫userinfo內容到檔案中達到紀錄的目的

> /AI_Web1?SID=sdkjcsssssjsd&Userinfo=eyAgImF1dGhvcml0eUFnZW50IjogIjAiLCAgImJvc2kiOi

## 測試連結API

網址後加如下測試
> /AI_API1/Test/GetUserinfo 
> /AI_API1/WeatherForecast

 ![enter image description here](https://raw.githubusercontent.com/gcl858/dotNetContainerSample1/main/images/%E8%9E%A2%E5%B9%95%E5%BF%AB%E7%85%A7%202023-11-08%2010-29-10.png)


## 基本command

docker exec -it "xxxxxx" bash

docker ps -a

docker logd -f

docker compose down

