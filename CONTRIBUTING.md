嗨，提前感谢你对mapbox gl 的贡献，这里讲述的是我们如何工作，请按约定提交 issue 或 pr 。

## 准备你的开发环境

### OSX

安装xcode命令行工具包
```bash
xcode-select --install
```

安装 [node.js 14](https://nodejs.org/)
```bash
brew install node@14
```
安装 [yarn](https://yarnpkg.com/en/)
```bash
brew install yarn
```

克隆这个仓库
```bash
git clone git@github.com:mapbox/mapbox-gl-js.git
```

安装仓库依赖
```bash
yarn install
```

### Linux

安装 [git](https://git-scm.com/), [node.js 14](https://nodejs.org/), [GNU Make](http://www.gnu.org/software/make/), 和 libglew-dev
```bash
sudo apt-get update
curl -sL https://deb.nodesource.com/setup_14.x | sudo bash -
sudo apt-get install build-essential git nodejs libglew-dev libxi-dev
```

安装 [yarn](https://yarnpkg.com/en/docs/install#linux-tab)
```bash
curl -o- -L https://yarnpkg.com/install.sh | bash
```
(也可能在安装Debian/Ubuntu时安装了yarn. 参考 [yarn's install instructions](https://yarnpkg.com/en/docs/install#linux-tab)).

克隆仓库
```bash
git clone git@github.com:mapbox/mapbox-gl-js.git
```

安装依赖
```bash
yarn install
```

### Windows

安装 [git](https://git-scm.com/), [node.js 14](https://nodejs.org/), [yarn](https://yarnpkg.com/en/docs/install#windows-tab), [npm 和 node-gyp](https://github.com/Microsoft/nodejs-guidelines/blob/master/windows-environment.md#compiling-native-addon-modules).

克隆仓库
```bash
git clone git@github.com:mapbox/mapbox-gl-js.git
```


安装依赖
```bash
yarn install
```

安装依赖 headless-gl  https://github.com/stackgl/headless-gl#windows
```
copy node_modules/headless-gl/deps/windows/dll/x64/*.dll c:\windows\system32
```

## 启动调试页面

启动调试服务

```bash
MAPBOX_ACCESS_TOKEN={你申请的key} yarn run start-debug
```

在 [http://localhost:9966/debug](http://localhost:9966/debug) 打开调试页面

## 打包

打包可以将仓库的内容集中在  `mapbox-gl.js` 和 `mapbox-gl.css` 两个文件中，这可以在html页面中更方便的使用.

打包需要运行：
```bash
yarn run build-prod-min
yarn run build-css
```

一旦打包完成，便会生成 `dist/mapbox-gl.js` 和 `dist/mapbox-gl.css` 两个打包文件中

## 编写代码 & 运行测试

参考 [`test/README.md`](./test/README.md).

## 编写代码 & 运行原型（性能测试）

参考 [`bench/README.md`](./bench/README.md).

## 代码约定

* 我们使用 [`error` events（错误事件）](https://www.mapbox.com/mapbox-gl-js/api/#Map.event:error) 返回用户错误.
* 我们使用 [`assert`](https://nodejs.org/api/assert.html)来检查非用户错误引起的不变量。这些`assert`语句被从生产构建中剥离出来。
* 我们使用一下es6的特性:
  * `let`/`const`
  * `for...of` 循环
  * 箭头函数
  * Class 类
  * 模板字符串
  * 计算和简写对象属性
  * 默认参数
  * 剩余参数
  * 解构
  * 模块
  * `...`
  * 迭代器和生成器
  * `Map`, `Set`, `array.find` 等.

导出模块约定如下:

* 不导出命名空间对象 -- 模块导出应是 类（classes）或 函数（functions）, 以及根据需要偶尔的异常.
* 如果导出模块和文件名相同 (模块的情况下), 它应该是默认导出的.
* 任何东西都需要一个命名导出.

### 版本控制如下

* 我们使用 [rebase merging](https://git-scm.com/book/en/v2/Git-Branching-Rebasing) (而不是 [basic merging](https://git-scm.com/book/en/v2/Git-Branching-Basic-Branching-and-Merging#Basic-Merging)) 合并分支

以下是推荐的获得设置的方式:
1. fork仓库
2. 克隆fork的仓库, `git clone git@github.com:GithubUser/mapbox-gl-js.git`
3. `cd mapbox-gl-js`
4. 添加官方仓库作为上游仓库: `git remote add upstream git@github.com:mapbox/mapbox-gl-js.git`
5. 为你的贡献建立新的分支 `git checkout -b your-branch`
6. 编写代码，当准备好时从你的分支上打开一个PR
7. 如果需要解决PR分支与主分支的冲突，你需要: `git fetch upstream`, `git rebase upstream/main` 并且强行推送到GitHub上 `git push --force origin your-branch`

## 更新日志约定（以下为纯机翻）

`CHANGELOG.md` 是许多人阅读且有价值的文件。它包含一个格式化的轻微编辑的项目历史。以拉请求为改变的单位，在审查时通常被分类和总结。通过将自动化内容搜索和格式化与最终人类编辑组合来维护更改内容。

如何保证更改日志条目?

- 影响公共API，视觉外观或用户安全性的任何更改必须*具有更改内容条目
- 任何绩效改进或错误修复*应该*有一个变更词
- 社区成员*可能*的任何贡献*都有一个更加平兴的条目，无论多么小（伴随着最终的变更歌曲: `(h/t [<user>](https://github.com/<user>))`)
- 任何文档相关的更改*不应该*有一个更改的条目
- 在同一版本中引入和修复的任何回归变更*不应该*具有更改内容
- 任何内部重构，技术债务减少，渲染测试，单位测试或基准相关变更*不应*具有更改内容

如何添加你的变更记录？ChangeLog条目是写在Pr模板中的`<changelog></changelog>`标记内。更长孔条目应该：


- 是描述性和简洁的;它应该解释没有上下文的读者的变化
- 描述表面错误，而不是潜在的问题。这可能需要一些研究。.
- 如果PR对最终用户没有影响，则被标记为`Skip ChangeLog`，并且不需要更改日志条目
- 被标记为`breaking change`如果PR是破坏的变化
- 引用PR和可选的问题.

## 文档约束

从 [`mapbox-gl-js-docs`](https://github.com/mapbox/mapbox-gl-js-docs/) 参考[`README.md`](https://github.com/mapbox/mapbox-gl-js-docs/blob/publisher-production/README.md).

### Github Issue 标签

我们的标签系统是

 - **minimalistic:** 标签的有用性与我们有多少成反比成反比.
 - **objective:** 标签应该是有目的，以至于任何两个人都会就标签决定一致.
 - **useful:** 标签应该跟踪状态或捕获语义含义，否则将很难搜索.

我们将我们的标签划分为类别，使他们更容易使用.

 - type (blue)
 - actionable status (red)
 - non-actionable status (grey)
 - importance / urgency (green)
 - topic / project / misc (yellow)

## 推荐阅读

### 学习 WebGL

- [Greggman's WebGL articles](http://webglfundamentals.org/)
- [WebGL reference card](http://www.khronos.org/files/webgl/webgl-reference-card-1_0.pdf)

### GL 性能表现

- [Debugging and Optimizing WebGL applications](https://docs.google.com/presentation/d/12AGAUmElB0oOBgbEEBfhABkIMCL3CUX7kdAPLuwZ964)
- [Graphics Pipeline Performance](http://developer.download.nvidia.com/books/HTML/gpugems/gpugems_ch28.html)

### 杂项

- [Drawing Antialiased Lines with OpenGL](https://blog.mapbox.com/drawing-antialiased-lines-with-opengl-8766f34192dc)
- [Drawing Text with Signed Distance Fields in Mapbox GL](https://blog.mapbox.com/drawing-text-with-signed-distance-fields-in-mapbox-gl-b0933af6f817)
- [Map Label Placement in Mapbox GL](https://blog.mapbox.com/map-label-placement-in-mapbox-gl-c6f843a7caaa)
- [Signed Distance Fields](http://bytewrangler.blogspot.com/2011/10/signed-distance-fields.html)
