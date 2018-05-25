## axios-upload
node 中在 axios 基础上上传表单数据

![npm](https://img.shields.io/npm/v/axios-upload.svg)
![npm](https://img.shields.io/npm/dm/axios-upload.svg)

[![GitHub forks](https://img.shields.io/github/forks/JYFiaueng/axios-upload.svg?style=social&label=Fork)](https://github.com/JYFiaueng/axios-upload/fork)
[![GitHub stars](https://img.shields.io/github/stars/JYFiaueng/axios-upload.svg?style=social&label=Star)](https://github.com/JYFiaueng/axios-upload)

### Installation
```
npm i axios-upload 
```

### example
```
const axiosUpload = require('axios-upload');

// 这里直接将 stream 传入即可
const data = {
  name: 'test',
  filedata: fs.createReadStream('./test.png')
};

await axiosUpload({
  url: 'http://xxx.xxx/test',
  method: 'post',
  headers: {
    'cache-control': 'no-cache'
  },
  data: data
});
```