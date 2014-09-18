# 集成开发解决方案 - 前端系列


## 说明

- 此文档从建立到逐步完善是一个长期过程
- 文档的覆盖面比较广，将会设计到开发-部署-测试-流程-规范等方方面面


## 参考文章

*TODO*

## ChangeLog

*TODO*

## 目录

- 1 开发规范
- 2 模块化开发
- 3 组件化开发
- 4 组件仓库
- 5 性能优化
- 6 项目部署
- 7 开发流程
- 8 开发工具
- 9 质量保证

## 正文

### 1 [开发规范](dev-guide.md)

包括开发、部署的目录规范，编码规范等。不要小瞧规范的威力，可以极大的提升开发效率，真正优秀的规范不会让使用者感到约束，而是能帮助他们快速定位问题，提升效率。

### 2 [模块化开发](modularization.md)

针对js、css，以功能或业务为单元组织代码。js方面解决独立作用域、依赖管理、api暴露、按需加载与执行、安全合并等问题，css方面解决依赖管理、组件内部样式管理等问题。是提升前端开发效率的重要基础。现在流行的模块化框架有requirejs、seajs等。

### 3 [组件化开发](componentization.md)

在模块化基础上，以页面小部件(component)为单位将页面小部件的js、css、html代码片段放在一起进行开发、维护，组件单元是资源独立的，组件在系统内可复用。比如头部(header)、尾部(footer)、搜索框(searchbar)、导航(menu)、对话框(dialog)等，甚至一些复杂的组件比如编辑器(editor)等。通常业务会针对组件化的js部分进行必要的封装，解决一些常见的组件渲染、交互问题。

### 4 [组件仓库](component-repo.md)

有了组件化，我们希望将一些非常通用的组件放到一个公共的地方供团队共享，方便新项目复用，这个时候我们就需要引入一个组件仓库的东西，现在流行的组件库有bower、component等。团队发展到一定规模后，组件库的需求会变得非常强烈。

### 5 [性能优化](po.md)

这里的性能优化是指能够通过工程手段保证的性能优化点。性能优化是前端项目发展到一定阶段必须经历的过程。强调的一点是 **性能优化一定是一个工程问题和统计问题** ，不能用工程手段保证的性能优化是不靠谱的，优化时只考虑一个页面的首次加载，不考虑全局在宏观统计上的优化提升也是片面的。

### 6 [项目部署](deploy.md)

部署按照现行业界的分工标准，虽然不是前端的工作范畴，但它对性能优化有直接的影响，包括静态资源缓存、cdn、非覆盖式发布等问题。合理的静态资源资源部署可以为前端性能带来较大的优化空间。

### 7 [开发流程](workflows.md)

完整的开发流程包括本地开发调试、视觉效果走查确认、前后端联调、提测、上线等环节。对开发流程的改善可以大幅降低开发的时间成本，很多独立的系统（cms系统、静态资源推送系统）将开发流程割裂开，对前端开发的效率有严重的阻碍。

### 8 [开发工具](build.md)

里说的工具不是指IDE，而是指工程工具，包括构建与优化工具、开发-调试-部署等流程工具，以及组件库获取、提交等相关工具，甚至运营、文档、配置发布等平台工具。前端开发需要工具支持，这个问题的根本原因来自前端领域语言特性。前端开发所使用的语言（js、css、html）以及前端工程资源的加载与定位策略决定了前端工程必须要工具支持。由于这些工具通常都是独立的系统，要想把它们串联起来，才有了yeoman这样的封装。前面提到的7项技术元素都直接或间接的对前端开发工具设计产生一定的影响，因此能否串联其他技术要素，使得前端开发形成一个连贯可持续优化的开发体系，工具的设计至关重要。

可参考的构建工具，
- [yeoman](http://yeoman.io/)
- [F.I.S](http://fis.baidu.com/)
- [gulp](http://gulpjs.com/)

### 9 [质量保证](qa.md)

测试覆盖、单元测试、自动化测试


----------



其中，
- 1-3（ 开发规范 、 模块化开发 、 组件化开发 ）是 **技术和业务相关的开发需求**
- 4（ 组件仓库 ）是 技术沉淀与共享需求
- 5-9（ 性能优化 、 项目部署 、 开发流程 、 开发工具 、 质量保证 ）是 **工程优化需求**
