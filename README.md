<<<<<<< HEAD
# bpmn-js Modeler + Properties Panel Example

This example uses [bpmn-js](https://github.com/bpmn-io/bpmn-js) and [bpmn-js-properties-panel](https://github.com/bpmn-io/bpmn-js-properties-panel). It implements a BPMN 2.0 modeler that allows you to edit execution related properties via a properties panel.


## About

This example is a node-style web application that builds a user interface around the bpmn-js BPMN 2.0 modeler.

![demo application screenshot](https://raw.githubusercontent.com/bpmn-io/bpmn-js-examples/master/properties-panel/docs/screenshot.png "Screenshot of the modeler + properties panel example")


## Usage

Add the [properties panel](https://github.com/bpmn-io/bpmn-js-properties-panel) to your project:

```
npm install --save bpmn-js-properties-panel
```

Additionally, if you'd like to use [Camunda BPM](https://camunda.org) execution related properties, include the [camunda-bpmn-moddle](https://github.com/camunda/camunda-bpmn-moddle) dependency which tells the modeler about `camunda:XXX` extension properties:

```
npm install --save camunda-bpmn-moddle
```

Now extend the [bpmn-js](https://github.com/bpmn-io/bpmn-js) modeler with two properties panel related modules, the panel itself and a provider module that controls which properties are visible for each element. Additionally you must pass an element via `propertiesPanel.parent` into which the properties panel will be rendered (cf. [`app/index.js`](https://github.com/bpmn-io/bpmn-js-examples/blob/master/properties-panel/app/index.js#L16) for details).

```javascript
var propertiesPanelModule = require('bpmn-js-properties-panel'),
    // providing camunda executable properties, too
    propertiesProviderModule = require('bpmn-js-properties-panel/lib/provider/camunda'),
    camundaModdleDescriptor = require('camunda-bpmn-moddle/resources/camunda');

var bpmnModeler = new BpmnModeler({
  container: '#js-canvas',
  propertiesPanel: {
    parent: '#js-properties-panel'
  },
  additionalModules: [
    propertiesPanelModule,
    propertiesProviderModule
  ],
  // needed if you'd like to maintain camunda:XXX properties in the properties panel
  moddleExtensions: {
    camunda: camundaModdleDescriptor
  }
});
```


## Building the Example

You need a [NodeJS](http://nodejs.org) development stack with [npm](https://npmjs.org) and installed to build the project.

To install all project dependencies execute

```
npm install
```

Build the example using [browserify](http://browserify.org) via

```
npm run all
```

You may also spawn a development setup by executing

```
npm run dev
```

Both tasks generate the distribution ready client-side modeler application into the `dist` folder.

Serve the application locally or via a web server (nginx, apache, embedded).
=======
# bpmnjs

#### 介绍
用于生成Acticiti7中使用的bpmn文件

#### 软件架构
软件架构说明


#### 安装教程

1.  xxxx
2.  xxxx
3.  xxxx

#### 使用说明

1.  xxxx
2.  xxxx
3.  xxxx

#### 参与贡献

1.  Fork 本仓库
2.  新建 Feat_xxx 分支
3.  提交代码
4.  新建 Pull Request


#### 特技

1.  使用 Readme\_XXX.md 来支持不同的语言，例如 Readme\_en.md, Readme\_zh.md
2.  Gitee 官方博客 [blog.gitee.com](https://blog.gitee.com)
3.  你可以 [https://gitee.com/explore](https://gitee.com/explore) 这个地址来了解 Gitee 上的优秀开源项目
4.  [GVP](https://gitee.com/gvp) 全称是 Gitee 最有价值开源项目，是综合评定出的优秀开源项目
5.  Gitee 官方提供的使用手册 [https://gitee.com/help](https://gitee.com/help)
6.  Gitee 封面人物是一档用来展示 Gitee 会员风采的栏目 [https://gitee.com/gitee-stars/](https://gitee.com/gitee-stars/)
>>>>>>> 7316ed89748d4008509101a199558c3ec460294a
