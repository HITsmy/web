### 前端API

端口：8081

### Admin
login 函数需求
{

    1. 成功需要返回的类型
    {
        "code":20000,
        "data":{"token":"admin-token"}
    }
    +
    2.失败需要返回的类型
    {
        "code": 60204,
        "message": "Account and password are incorrect."
    }
}