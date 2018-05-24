## axios-upload
node 中在 axios 基础上上传表单数据

### Installation
npm i axios-upload 

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