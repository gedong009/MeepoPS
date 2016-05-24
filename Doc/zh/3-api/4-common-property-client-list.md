# 接口的通用属性: clientList

- 名称: instanceName.
- 类型: string.
- 描述: instanceName用来设置这个实例(接口类的对象)的名称.
- 提示: 设置后在查看运行状态时会比较方便. 比如实例一监听19910端口用来接收游戏聊天数据, 实例二监听19911端口用来接收服务器负载信息, 那么在查看状态的时候我们可能会混淆不同实例的作用.
- 备注: 这里设置了名称后, 查看FastWS的状态时会显示, 同事FastWS会根据这个名称来设置系统的进程名称. 但是Mac不能设置进程名称无效. Linux用户可以使用ps来查看进程名称.
- 示例: 
这是我们自行编写的业务逻辑代码: demo.php
```php
//引入FastWS
require_once 'FastWS/index.php';

//使用文本传输的Telnet接口类
$telnet = new \FastWS\Api\Telnet('0.0.0.0', '19910');

//设置FastWS实例名称
$telnet->instanceName = 'FastWS-Telnet';

//启动FastWS
\FastWS\runFastWS();
```