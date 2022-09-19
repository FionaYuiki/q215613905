# q215613905-Tbox
复刻自TG群俊于phper的库：https://github.com/q215613905/TVBoxOS/ 


1、修改软件名称地址
https://github.com/dabbing2019/TVBoxOS/blob/main/app/src/main/res/values/strings.xml

2、修改版本号
https://github.com/dabbing2019/TVBoxOS/blob/main/app/src/main/AndroidManifest.xml

3、修改图标、背景
https://github.com/dabbing2019/TVBoxOS/tree/main/app/src/main/res


4、修改内置源
俊老仓库打开下面,第83行
https://github.com/dabbing2019/TVBoxOS/blob/main/app/src/main/java/com/github/tvbox/osc/api/ApiConfig.java
takagen99大佬仓库 改这里;app/src/main/res/values-zh/strings.xml


5、修改默认缩略图、硬解、dns
地址：
https://github.com/dabbing2019/TVBoxOS/blob/main/app/src/main/java/com/github/tvbox/osc/base/App.java

代码
@@ -53,9 +53,19 @@ private void initParams() {
        if (!Hawk.contains(HawkConfig.PLAY_TYPE)) {
            Hawk.put(HawkConfig.PLAY_TYPE, 1);
        }
        //自定义默认配置-硬解-安全dns-缩略图
        if (!Hawk.contains(HawkConfig.IJK_CODEC)) {
            Hawk.put(HawkConfig.IJK_CODEC, "硬解码");
        }
        if (!Hawk.contains(HawkConfig.DOH_URL)) {
            Hawk.put(HawkConfig.DOH_URL, 2);
        }
        if (!Hawk.contains(HawkConfig.SEARCH_VIEW)) {
            Hawk.put(HawkConfig.SEARCH_VIEW, 2);
        }
    }

    public static App getInstance() {
        return instance;
    }
