# ChangeLocation
改变自己的定位地址。


## 使用步骤：
1. 修改Location1.gpx的位置；
2. 将demo运行至手机；
3. 在运行状态下，将Xcode调至，点击Debug--->Simulate Location --> Location1（这个是你创建gpx的文件名哦）；
4. 再来看你的手机系统位置。




## 后续说明
##### 必须连接上真机。然后运行。
运行后，点击Debug--->Simulate Location --> Location1（这个是你创建gpx的文件名哦）
这时你会发现手机当前的定位已经切换到你的经纬度。

你要修改另一个位置，只需要重新修改gpx中的参数，然后重新运行，发现还是上次的位置。这个时候只需要再点Location1，就可以更新到最新位置。


## 地图坐标系
在地图开发中：我们会接触到3中类型的地图坐标系：
1. WGS－84原始坐标系，一般用国际GPS纪录仪记录下来的经纬度，通过GPS定位拿到的原始经纬度，Google和高德地图定位的的经纬度（国外）都是基于WGS－84坐标系的；但是在国内是不允许直接用WGS84坐标系标注的，必须经过加密后才能使用；
2. GCJ－02坐标系，又名“火星坐标系”，是我国国测局独创的坐标体系，由WGS－84加密而成，在国内，必须至少使用GCJ－02坐标系，或者使用在GCJ－02加密后再进行加密的坐标系，如百度坐标系。高德和Google在国内都是使用GCJ－02坐标系，可以说，GCJ－02是国内最广泛使用的坐标系；
3. 百度坐标系:bd-09，百度坐标系是在GCJ－02坐标系的基础上再次加密偏移后形成的坐标系，只适用于百度地图。(目前百度API提供了从其它坐标系转换为百度坐标系的API，但却没有从百度坐标系转为其他坐标系的API)
而我们iOS端采用的定位坐标系是WGS-84.
