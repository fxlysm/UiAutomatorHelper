##Uiautomator测试调试

###进入工程目录###

android create uitest-project -n sample -t 4 -p C:\KAZAM\AutoTest\Sample


ant -buildfile build.xml


adb push C:\KAZAM\AutoTest\Sample\bin\Sample.jar  data/local/tmp/



adb shell uiautomator runtest Sample.jar  -c  kazam.autotest

或者
adb shell uiautomator runtest Sample.jar  -c  kazam.autotest#test  -c  kazam.autotest#testkey



adb shell uiautomator runtest  autotest.jar --nohup -c  kazam.settings.about_phone  -c kazam.settings.audio_profiles  -c kazam.settings.Switch_language  -c kazam.launcher.unlockTestcase  -c kazam.launcher.Quick_settings  -c kazam.camera.camera_takepicture   -c kazam.camera.camera_settings  


