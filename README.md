# coss 批量自转脚本

## 安装

```
yarn install
```
修改 .env.example 为 .env

## 配置环境变量
在项目根目录中创建 .env 文件，并填写以下信息：
```
//可以去 blockpi找
NODE_URL=
PRIVATE_KEY=
```

## 钱包批量生成
```
node wallet_gen.js
```

代码里面可以调整生成的个数

## 批量转账

```
node transfer.js
```
请先执行批量生成，然后再执行批量转账
默认给生成的 cosmos_wallets.json 里面所有的地址转1个ATOM ，请按需调整

## 批量mint
用cosmos_wallets.json里的所有地址来mint，没有的话按相同格式自行添加
```
node index.js
```
