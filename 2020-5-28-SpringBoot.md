1. ## Maven的Scope区别和描述

   * compile
     默认scope为compile，表示为当前依赖参与项目的编译、测试和运行阶段，属于强依赖。打包之时，会达到包里去。
   * test
     该依赖仅仅参与测试相关的内容，包括测试用例的编译和执行。
   * runtime
     依赖仅参与运行周期中的使用。一般这种类库都是接口与实现相分离的类库，
   * provided
     该依赖在打包过程中，不需要打进去，这个由运行的环境来提供。
   * system
     使用上与provided相同，不同之处在于该依赖不从maven仓库中提取，而是从本地文件系统中提取，其会参照systemPath的属性进行提取依赖。
   * import
     这个是maven2.0.9版本后出的属性，import只能在dependencyManagement的中使用，能解决maven单继承问题，import依赖关系实际上并不参与限制依赖关系的传递性

2. ## 描述Spring  @Configuration @Bean @ComponentScan @PropertySource @Value注解

   1、@Configuration作用于类上，相当于一个xml配置文件；
   2、@Bean作用于方法上，相当于xml配置中的<bean>；

   3、@ComponentScan //配置指定的扫描包

   4、@PropertySource可以指定读取的配置文件，

   6、@Value注解获取值

3. ## 什么是SpringBoot,优点和缺点?

   * Spring Boot 是 Spring 开源组织下的子项目，是 Spring 组件一站式解决方案，主要是简化了使用 Spring 的难度，简省了繁重的配置，提供了各种启动器，开发者能快速上手 

     优点：

     * 快速构建项目

     * 对主流开发框架的无配置集成项目可独立运行，无需外部依赖 Servlet 容器

     * 提供运行时的应用监控

     * 极大地提高了开发、部署效率

     * 与云计算的天然集成

       缺点：

       1. 版本迭代速度很快，一些模块改动很大

       2. 由于不用自己做配置，报错时很难定位

4. ## 什么是yml? 语法格式（说3点)

    YAML 是一种人类可读的数据序列化语言。它通常用于配置文件。与属性文件相比，如果我们想要在配置文件中添加复杂的属性，YAML 文件就更加结构化，而且更少混淆。可以看出 YAML 具有分层配置数据。 

   1. 使用缩进表示层级关系
   2. 缩进时不允许使用Tab键，只允许使用空格
   3. 缩进的空格的数目不重要，只要相同层级的元素左对齐即可
   4. 大小写敏感

5. ## SpringBoot(4个注解)并说明其作用

   @SpringBootConfiguration：组合了 @Configuration 注解，实现配置文件的功能。

   @EnableAutoConfiguration：打开自动配置的功能，也可以关闭某个自动配置的选项，如关闭数据源自动配置功能： @SpringBootApplication(exclude = { DataSourceAutoConfiguration.class })。

   @ComponentScan：Spring组件扫描。

6. ## Spring Boot 的核心注解是哪个？主要由哪几个注解组成的？

   @SpringBootApplicatio

   * @SpringBootConfiguration
   * @EnableAutoConfiguration
   * @ComponentScan

7. ## Spring-boot-maven-plugin插件作用

   ```
   可以使用Java -jar命令来启动jar包，并且有了这个插件，
   打的包里面才会有maven依赖的jar包和spring boot的启动类，所以打的jar包也就比较大
   ```

8. ## Springboot自动配置的原理

   注解 @EnableAutoConfiguration, @Configuration, @ConditionalOnClass 就是自动配置的核心，

   @EnableAutoConfiguration 给容器导入META-INF/spring.factories 里定义的自动配置类。

   筛选有效的自动配置类。

   每一个自动配置类结合对应的 xxxProperties.java 读取配置文件进行自动配置功能

9. ## **Springboot读取配置文件的方式** 

   

10. ## application 和 bootstrap 配置文件的区别