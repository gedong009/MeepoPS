# Telnet协议

Telnet协议是一个应用层协议, 是指像telnet客户端一样收发消息. 每个消息之间用换行符("\n")分割.

每个数据包已\n来结尾. 如果发现\n, 则\n之前为一个数据包. 如果没有\n, 则等待下次数据的到来.

在接收到一个链接发来的消息后, MeepoPS会删除最后的\n, 然后才会将数据发送给您.

在给一个链接发送消息时, MeepoPS会自动帮您在结尾添加\n, 以便客户端可以识别. 不需要您手动添加.