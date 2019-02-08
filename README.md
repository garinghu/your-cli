# your-cli
一个可自定义模版库的cli

看vue-cli源码的时候手痒打算写个简单的cli玩玩，于是想到自己在git上的一些模版用的时候都要clone很麻烦，这个cli可以提前注册好要用的模版，想用的时候直接通过命令行即可创建，感觉还有点实用。


## 用法

### install

```
sudo npm install your-cli -g

```

### 注册模版库

```
your-add

```
这时会提示输入远程模版库的地址和别名（再次加载时会通过别名选择），然后会判断模版库中是否有package.json文件，如果包含，则进行模版化改造（暂时支持最基础的定制name，version，description）。

### init

```
your-init

```
会提示选择已经注册的模版库别名，选择后就会出现在当前文件夹，然后输入项目名称、版本和描述。


## 备注
引入了metalsmith结合handlebars进行模版改造，暂时支持定制name，version，description。