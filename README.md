# iscs
intergrated supervisory control sysytem

#### 积累：
##### 1.设计模式记录：
  - 工厂模式为建立接口实现类，类似的类均实现接口类，再创建工厂类，根据不同参数返回具体类；
  - 抽象工厂模式为建立抽象类，类似的类扩展抽象类，再创建工厂生产类，根据不同参数返回具体工厂实现的类；
  - 单例模式为只能有一个实例，private static Singleton instance;  无论创建多次都仅有一个实例；
  - 建造者模式为builder用于多参数创建时带来便利；
  - 原型模式是创建一个实现了 Cloneable 接口的抽象类，通过同类型实现该抽象类；
  - 适配器模式





##### 2.记录好的代码习惯：
 - public String toString() {return new Gson().toJson(this);}
 - implements Serializable，设置uid
 - @PostConstruct
   public void setup() {
        this.mappings = Maps.newConcurrentMap();
        this.mappings.put(ConveyorStateMutation.class,conveyorStateMutator);}
 - StringUtils.replaceAll;
 - DateUtils.truncate(new Date(), Calendar.DATE);零点时刻；
 - implements InitializingBean，@Override public void afterPropertiesSet() throws Exception；
 - Stopwatch  Spring计时器；
 - public String toJson(){JSONObject jsonObject = new JSONObject;jsonObject.put("aa",aa)...;return jsonObject.toJSONObject;}；
 - 函数式接口@FunctionalInterface；
##### 3.IDEA插件
 - https://plugins.jetbrains.com/plugin/4946-simpleumlce
 - https://plugins.jetbrains.com/plugin/7017-plantuml-integration
 - https://plugins.jetbrains.com/plugin/7179-maven-helper
 - https://plugins.jetbrains.com/plugin/1800-database-navigator
 - https://confluence.jetbrains.com/display/CONTEST/Database+Navigator
 - https://plugins.jetbrains.com/plugin/7141-mongo-plugin
 - https://plugins.jetbrains.com/plugin/7654-gsonformat
 - https://plugins.jetbrains.com/plugin/4230-bashsupport

##### 4.REACT学习笔记
 - 创建组件，需要class Child extends React.Compent{};
 - 渲染需要用ReactDOM.render;
 - 只要导入react.js和react-dom.js就可以是react工程；
 - React.createElement创建一个元素，里面参数有多种形式；
 - this.props为渲染不同的文本，被调用时所有属性都会被传递过去；
 - 
##### 5.spring
 - 配置selvet,入口核心类dispatcherServlet，方法为doDispatch;
 - spring mvc对接tomcat入口为FrameWorkServlet,方法为service；
 
 ##### 6.解析xml
 - 获取文件路径：this.getClass.getResource("/");
 - 替换：String.replaceAll;
 - 解析：new SAXBuilder;
 - 解析结果获取节点：.getChildren

##### 7.设计模式
 - 观察者模式：一个变化，依赖他的对象变化都得到通知并被更新；即变化利用事件的方式：调用时new事件对象，通过注入applicationContext,方法为publishEvent创建一个事件；自定义事件，实现applicationEvent；创建监听类并实现applicationListener，监控可做出相应的动作；也可以用smartApplicationListener可以关心事件后的执行顺序；可以随便产生事件，也可多个监听器；
 - 策略模式：一些列算法封装起来，他们可以相互替换，让算法独立于使用它的客户；具体方式：定义抽象类或接口，从而可以替换的是接口实现或子类；
 - 组合模式：spring特性：在类的结构函数中定义List<具体接口>，则默认将所有这个接口的实现类，放到这个List里面去，结构函数内可对List做for循环，放到Map中，可随时通过名字获取到对应的实现类；
