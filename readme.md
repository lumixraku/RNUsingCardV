

# 使用自定义 RN Package 的例子

自定义 RN Native Package 在这里  https://github.com/lumixraku/react-native-cardv

参考

https://medium.com/wix-engineering/creating-a-native-module-in-react-native-93bab0123e46

https://github.com/quenice/react-native-cardview

# Why ?
官方 https://reactnative.dev/docs/native-modules-setup  这里介绍的方式行不通, 存在报错循环 .

通过这个命令创建的package 在引入到的项目并import 的时候会有下面的问题


### React-Native Module HMRClinet is not a registered callable module(calling enable)
https://thetopsites.net/article/50618528.shtml
https://stackoverflow.com/questions/54935132/module-hmrclient-is-not-registered-react-native-why-is-this-happening-and-how-t
https://stackoverflow.com/questions/53220633/module-hmrclient-is-not-a-registered-callable-module-calling-enable-in-linux


### React Native:Module RCTDeviceEventEmitter is not a registered callable module (calling emit)
https://github.com/facebook/react-native/issues/27193
https://github.com/joltup/react-native-threads/issues/40

尝试了所有的帖子中所有的办法都未能解决.


## install
在本地用 react-native-create-library 创建好一个repo, 比如我这里叫做 react-native-cardv

yarn add /Users/lilin/repos/RN/react-native-cardv 引入到你的项目中

在 add 的过程中就会build 你的native repo
```
[1/4] 🔍  Resolving packages...
[2/4] 🚚  Fetching packages...
[3/4] 🔗  Linking dependencies...
[4/4] 🔨  Building fresh packages...

```


另外第一次引入的话, 仍然需要手动link  `npx react-native link react-native-cardv`
```
import CardV from 'react-native-cardv'
Cardv.show(...)
```