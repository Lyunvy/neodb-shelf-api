## 获取自己 NeoDB 上的项目内容
1. 在 [NeoDB API Developer Console](https://neodb.social/developer/) 获取 Access Token；
2. 在 vercel 上部署该项目，设置环境变量 `AUTHORIZATION` 为第一步获取的 Access Token；
3. 部署成功后，访问 https://yourdomain/api?type={type}&category={category} ，`{type}` 为 `wishlist / progress / complete` ，`{category}` 为 `book / movie / tv / music / game / podcast`，可以获得 json 数据。

## 在本地测试
1. 将 https://github.com/Lyunvy/neodb-shelf-api/blob/9e42e260d064be9ab02dc73d2673609e971394e0/api/index.py#L15 改为
   ```python
   headers = {'Authorization': 'Bearer xxx', 'Accept': 'application/json'}
   ```
   其中 `xxx` 替换为 Access Token。
2. 将以下几行代码取消注释 https://github.com/Lyunvy/neodb-shelf-api/blob/9e42e260d064be9ab02dc73d2673609e971394e0/api/index.py#L47-L54
3. 在项目文件夹打开终端，依次执行
   ```shell
   pip install -r requirements.txt
   python api/index.py
   ```
4. 访问 http://127.0.0.1:8080/?type={type}&category={category} ，`{type}` 为 `wishlist / progress / complete` ，`{category}` 为 `book / movie / tv / music / game / podcast`，可以获得 json 数据。
