1、安装
    下载node安装8版本（最新），查看node版本和npm版本
    node -v 
    npm -v 

    npm安装vue和vue-cli
    npm install vue -g
    npm install vue-cli -g
    查看vue版本
    vue -V
2、创建项目
    （1）目录：D：\myCode
    （2）vue init webpack todolist(项目名称)
    （3）cd todolist (进入创建的项目目录)
    （4）npm install  （安装所有package.json文件中的依赖）
    （5）npm run dev / npm run start  (打开localhost：8080端口)    
         安装npm install 报错:（一般报错先检查版本是否兼容）
         npm install出现: Unexpected end of JSON input while parsing near
         解决方案：
         npm -g i npm@4  （重新安装4版本，5以上版本会有冲突异常）
         npm cache clean --force

    
