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
 - 
