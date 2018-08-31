# Fast Android快速开发
## 一、各种第三方框架
1、[ThreenTenABP](https://github.com/JakeWharton/ThreeTenABP)
>ThreeTenABP是针对Android系统优化过的 JSR-310兼容版本，相对于threetenbp，ThreeTenABP主要解决了ClassLoader.getResourceAsStream() 在Android中的内存问题JSR-310 API在很多地方沿袭了Joda Time的设计，比如最核心的几个概念： Instant, LocalDate, LocalTime, DateTime, Period, Duration等（Joda Time的创建者也是JSR-310的primary author) 同时又改进了Joda Time的几个缺陷.  

2、activity或fragment 路由跳转框架  
>（1）[ARouter](https://github.com/alibaba/ARouter)  
>>支持功能
>>1. 支持直接解析URL进行跳转、参数按类型解析到Bundle，支持Java基本类型(*)  
>>2. 支持应用内的标准页面跳转，API接近Android原生接口
>>3. 支持多模块工程中使用，允许分别打包，包结构符合Android包规范即可(*)
>>4. 支持跳转过程中插入自定义拦截逻辑，自定义拦截顺序(*)
>>5. 支持服务托管，通过ByName,ByType两种方式获取服务实例，方便面向接口开发与跨模块调用解耦(*)
>>6. 映射关系按组分类、多级管理，按需初始化，减少内存占用提高查询效率(*)
>>7. 支持用户指定全局降级策略
>>8. 支持获取单次跳转结果
>>9. 丰富的API和可定制性
>>10. 被ARouter管理的页面、拦截器、服务均无需主动注册到ARouter，被动发现
>>11. 支持Android N推出的Jack编译链  

>>不支持的功能  
>>1. 自定义URL解析规则(考虑支持)
>>2. 不能动态加载代码模块和添加路由规则(考虑支持)
>>3. 多路径支持(不想支持，貌似是导致各种混乱的起因)
>>4. 生成映射关系文档(考虑支持)  

>>典型应用场景  
>>1. 从外部URL映射到内部页面，以及参数传递与解析
>>2. 跨模块页面跳转，模块间解耦
>>3. 拦截跳转过程，处理登陆、埋点等逻辑
>>4. 跨模块API调用，模块间解耦(注册ARouter服务的形式，通过接口互相调用)  

>（2）[ActivityRouter](https://github.com/mzule/ActivityRouter)
