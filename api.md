[toc]

## API

端口号 : **Port:8080**

### LoginUserVo
实体类属性:
{
    username: String,
    password: String,
    identity: String,(admin or student)
}

### Admin 
实体类属性:
{
    name:String,
    password:String,
}
#### 1. login
+ url："/admin/login"
+ method: "Post"
+ request: {LoginUserVo} 
+ responce:
    1. 登录失败
    {
        code:20002,
        message:"用户名或密码错误"
    }
    2. 登陆成功:
    {
        code:20000,
        message:"success",
        data:"{adminToken}"
    }
#### 2. update Password
+ url: "/admin/Password"
+ method: "Put"
+ request: {Admin}
+ responce:
    1. 修改失败
    {
        code: 20003,
        message: "此用户不存在"
    }
    2. 修改成功
    {
        code: 20000,
        message: "修改成功"
    }
#### 3. get All Users
+ url: "/admin/users"
+ method: "Get"
+ request: null
+ responce: 
    1. 获取成功
    {
        code: 20004,
        message: "查询成功"
        data: {List of Users} 
    }
    2. 获取失败
    {
        code: 20000,
        message: "没有查询到用户"
    }

#### 4. get User By Name
+ url: "/admin/users/{username}"
+ method: "Get"
+ request: username: String
+ responce:
    1. 获取失败
    {
        code: 20004,
        message: "没有查询到用户"
    }
    2. 获取成功
    {
        code: 20000,
        message: "查询成功",
        data: {User}
    }
#### 5. reset User Password To Name
+ url: "users/{username}"
+ method: "Put"
+ request: username: String
+ responce:
    1. 重置失败
    {
        code: 20004,
        message: "没有查询到用户"
    }
    2. 重置成功
    {
        code: 20000,
        message: "重置成功",
    }
### Result
实体类属性:
{
    groupId: Integer,
    judgesName: String,
    score: double,
    workScore: double,
    cmtScore: double,
    uiScore: double,
    divScore: double
}
### Users
实体类属性:
{
    userName: String,
    realName: String,
    password: String,
    status: Integer,
    ifJudges: Integer,
    groupId: Integer
}


+ url:
+ method:
+ request:
+ responce:
