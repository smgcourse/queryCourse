# queryCourse 免费查课接口
公开免费查课接口，输入账号密码，返回课程列表

## 支持平台如下
| 平台名称 | type |
|------|------|
| 智慧树  | 1    |

## 请求地址 
```https://chake.world ```
## 请求参数

| 参数       | 说明           | 默认值   |
|----------|--------------|-------|
| school   | 学校名称(学号登陆必填) | -     |
| username | 账号或学号        | -     |
| password | 密码           | -     |
| plat     | 平台类型         | -     |
| detail   | 是否返回课程详细信息   | false |

## 请求说明

使用 HTTP ```GET```

| 名称 | 说明                                                   |
|---|------------------------------------------------------|
| 请求 URL  | https://chake.world?username=参数值&password=参数值&plat=1 |
|补充| 使用 GET 虽然简单, 但是你无法传入复杂的数据结构, 另外中文字符需要使用urlEncode编码   |

使用 HTTP ```POST```

| 名称 | 说明                                                |
|---|---------------------------------------------------|
| 请求 URL  | https://chake.world                           |
|请求体|请求体可以使用 JSON 也可以使用 Form 表单, 需要注意的是, 请求的 Content-Type 是一定要设置准确的|

HTTP POST JSON 格式
```json
{
    "username": "账号",
    "password": "密码",
    "school": "学校",
    "plat": 1
}

```
HTTP POST 表单格式
```
username=账号&password=密码&school=学校&plat=1
```
## 响应说明
