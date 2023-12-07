# coss 批量自转脚本

## 助记词转私钥
把你的助记词导入小青蛙钱包（leap wallet），然后导出私钥，然后私钥导入keplr钱包，然后就能在keplr看到你的私钥了
leap显示的私钥和keplr的不一样

## RPC
RPC 记得自己去 blockpi 申请，或者用公共的也可以。
https://github.com/cosmos/chain-registry/blob/7109d85fb58c8ac995a491912ddf9196834eda0b/cosmoshub/chain.json#L275

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

代码里面可以调整生成的个数，执行后会生成一个 cosmos_wallets.json 文件

## 批量转账

```
node transfer.js
```
请先执行批量生成，然后再执行批量转账
默认给生成的 cosmos_wallets.json 里面所有的地址转 1 个 ATOM ，请按需调整

## 批量mint
用 cosmos_wallets.json 里的所有地址来 mint，没有的话按相同格式自行添加
```
node index.js
```
