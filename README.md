# cocos2.x--newAudioEngine-
新的声音引擎移植到2.x引擎,可以和旧的混合使用
目录CocosDenshionAndroid放在和CocosDenshion同层。

Android 
Android.mk加入
1.LOCAL_WHOLE_STATIC_LIBRARIES  加上  audioengine_static
2.$(call import-module,CocosDenshionNew/android)

Application.mk
1.APP_CPPFLAGS  加上 -std=c++11
2.NDK_TOOLCHAIN_VERSION := 4.8
3.APP_PLATFORM := android-9
4.使用NDK_R9d编译

代码修改地方
查看3.xAndroid部分
