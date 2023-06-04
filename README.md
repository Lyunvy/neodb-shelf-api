## 获取自己 NeoDB 上的项目内容
1. 在 [NeoDB API Developer Console](https://neodb.social/developer/) 获取 Access Token；
2. 在 vercel 上部署该项目，设置环境变量 `AUTHORIZATION` 为第一步获取的 Access Token；
3. 部署成功后，访问 https://yourdomine/api?type={type}&category={category} ，`{type}` 为 `wishlist / progress / complete` ，`{category}` 为 `book / movie / tv / music / game / podcast`，可以获得 json 数据。
