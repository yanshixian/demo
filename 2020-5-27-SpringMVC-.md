1. ## Java有什么缺点（至少3条）

   ```
   1、需要运行环境、不适合开发桌面应用程序
   2、由于为了跨平台的功能，为了极度的伸缩能力，所以极大的增加了产品的复杂性。
   3、JAVA是OOP语言，但是它适合的是BS系统，在WEB项目中JAVA的实力毋庸置疑，但是转到了底层的程序却无法同C++抗衡。
   4、乱码是JAVA的第一公敌
   5、无法定义一个好的标准使得开发时使用了框架，在新的程序员来到公司时必须先了解框架，延缓了开发的时间。
   ```

2. ## JAVA常见编码规范（说5条）

    命名风格  

   *  不能以下划线或美元符号开始，也不能以下划线或美元符号结束。 
   *  严禁使用拼音与英文混合的方式，更不允许直接使用中文的方式。 
   *  方法名、参数名、成员变量、局部变量都统一使用 lowerCamelCase 风格，必须遵从 驼峰形式 
   *  常量命名全部大写，单词间用下划线隔开，力求语义表达完整清楚，不要嫌名字长 
   *  类型与中括号紧挨相连来表示数组 
   *  包名统一使用小写，点分隔符之间有且仅有一个自然语义的英语单词。 
   *  杜绝完全不规范的缩写，避免望文不知义。 

3. ## 说出git 命令（至少说6个）并分别说出其含义

   * git init 初始化本地 git 仓库 
   *  git status 查看当前版本状态 
   *  git diff 显示所有未添加至 index 的变更 
   *  git add <path> 将该文件添加到缓存 
   *  git commit -m ‘xxx’ 提交 
   *  git log 显示日志 
   *  git show <commit> 显示某个提交的详细内容 
   *  git branch 显示本地分支 
   *  git checkout <branch> 切换分支 
   *  git remote -v 列出远程分支详细信息 
   *  git merge <branch> 合并分支到当前分支，存在两个 

4. ## Spring中如果发生循环注入会怎样？(a注入b b注入a)

   * Spring内部代码是当解析依赖注入关系的时候，先判断是不是 @Lazy Bean，如果是，则暂不解析该依赖，如果不是则会进行依赖Bean的查找，如果查找不到则会创建。但是在创建的时候，由于和需要注入的Bean有循环依赖关系，所以注入Bean创建失败。

     

5. ## SpringMVC中的Bean是线程安全的吗？ 说出你的解决方案？

   *  SpringMVC是默认单例模式的 ,当涉及到改变成员变量的时候就会产生线程不安全,最简单的解决方法是在Controller类上添加@scope("XXXX")注解实现多例 

6. ## SpringMVC的执行流程？

   （1）用户发送请求至前端控制器DispatcherServlet；
   （2） DispatcherServlet收到请求后，调用HandlerMapping处理器映射器，请求获取Handle；
   （3）处理器映射器根据请求url找到具体的处理器，生成处理器对象及处理器拦截器一并返回给DispatcherServlet；
   （4）DispatcherServlet 调用 HandlerAdapter处理器适配器；
   （5）HandlerAdapter 经过适配调用 具体处理器(Handler，也叫后端控制器)；
   （6）Handler执行完成返回ModelAndView；
   （7）HandlerAdapter将Handler执行结果ModelAndView返回给DispatcherServlet；
   （8）DispatcherServlet将ModelAndView传给ViewResolver视图解析器进行解析；
   （9）ViewResolver解析后返回具体View；
   （10）DispatcherServlet对View进行渲染视图（即将模型数据填充至视图中）
   （11）DispatcherServlet响应用户

7. ## @RequestBody 和@ResponseBody的区别

   * @RequestBody： 主要用来接收前端传递给后端的json字符串中的数据的(请求体中的数据的) 
   * @ResponseBody： 该注解用于将Controller的方法返回的对象，通过适当的HttpMessageConverter转换为指定格式后，写入到Response对象的body数据区 

8. ## @RequestParam和@PathViriable的区别

   * 请求路径上有个id的变量值，可以通过@PathVariable来获取 @RequestMapping(value = “/page/{id}”, method = RequestMethod.GET)

   * @RequestParam用来获得静态的URL请求入参 spring注解时action里用到。

9. ## @Resource和 @Autowired/ @Qualifier的区别

   * @Autowired 根据类型注入， 
   * @Resource 默认根据名字注入，其次按照类型搜索
   * @Autowired @Qualifie("userService") 两个结合起来可以根据名字和类型注入

10. ## @RequestMapping注解作用

    * ##  是一个用来处理请求地址映射的注解，可用于类或方法上。用于类上，表示类中的所有响应请求的方法都是以该地址作为父路径。 


