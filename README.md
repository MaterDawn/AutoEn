## Auto.js加密解密算法说明

### 对于较旧的版本:AES/CBC/PKCS5Padding
```
///////////////////////////////////////////////////
/////  AES/CBC/PKCS5Padding
///////////////////////////////////////////////////
Inspeckage_Hash:Algorithm(MD5) [com.example.script15668979885591.0.0main.js : d7cab65e8a05d0c7a208a71121f47089]-----
Inspeckage_Hash:Algorithm(MD5) [AA01AAC9-1ww : 5dcfad62436f743148c5ba5985ab8a57]-----

文件为工程文件：project.json：
key是 MD5(packageName + versionName + main)小写；
iv是 MD5(build_id + name)小写前16位；
```
### 对于最新版的Auto.js Pro8.0：
```
///////////////////////////////////////////////////
/////  AES/CBC/PKCS7Padding
///////////////////////////////////////////////////
在smali代码代码中可以直接搜到 AES/CBC/PKCS7Padding
具体逻辑在类：Lcom/stardust/autojs/engine/encryption/ScriptEncryption;
跑出的日志：
Inspeckage_Hash:Algorithm(MD5) [com.wbzspl.czsmls1.0.0.......js : 1c185384bb6860b6e13f0c4c302af890]-----
Inspeckage_Hash:Algorithm(MD5) [D2646AAC-18............ : 5013d1d1555ea1368e1cb5f443de0a5d]-----
Inspeckage_Crypto:SecretKeySpec(1c185384bb6860b6e13f0c4c302af890,AES) , Cipher[AES/CBC/PKCS7Padding]  IV: 5013d1d1555ea136 (c129cfae8ded4b8b , L2RRR/XxM2Ff1akOq5HmGbfS+CaaZGdkYIeiBWJPnJY=)-----
```

具体分析过程见：https://mp.weixin.qq.com/s/j-_IwtEpD0-7W2vpoMxBog
