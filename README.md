#危化品车辆检测

##需求

现有十二台摄像机,摄像机会捕获镜头内的危化品车辆，并向服务端发送警告。十二台摄像机安装在双向车道中间位置，可同时捕捉到两个方向的车辆，任何方向的车辆经过摄像机都会发出警告。发送的警告中没有车辆的任何信息。服务端需要在收到警告信息后判断车辆的行驶状况，根据车辆的行驶情况向MQ中推送该车的行驶状况(速度过慢、停车、倒车)。

###警告信息

```json
    {
      "DBAlarmID": "123456"
      "AlarmTime": "2006-01-02T15:04:05",
      "CameraID": "K693+980",
      "ThumbnailPath": "www.baidu.com/image"
    } 
```
