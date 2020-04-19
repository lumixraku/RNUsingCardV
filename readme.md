

# 使用自定义 RN Package 的例子

自定义 RN Package  https://github.com/lumixraku/react-native-cardv

参考

https://medium.com/wix-engineering/creating-a-native-module-in-react-native-93bab0123e46

https://github.com/quenice/react-native-cardview

# Why ?
官方 https://reactnative.dev/docs/native-modules-setup  这里介绍的方式行不通, 存在报错循环 .


## install
在本地用 react-native-create-library 创建好你的repo 后

yarn add /Users/lilin/repos/RN/react-native-cardv 引入到你的项目中

另外仍然需要手动link  `npx react-native link react-native-cardv`