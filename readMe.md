## 项目名称：快递管理控制台项目
采用二维数组方式存储快递
### 1. 管理员
  - 快递录入
    - 柜子位置（系统产生，不能重复）
    - 快递单号（输入）
    - 快递公司（输入）
    - 6位取件码（系统产生，不能重复）
  - 删除快递（根据单号）
  - 修改快递（根据单号）
  - 查看所有快递（遍历）
### 2. 普通用户
* 快递取出
    * 输入取件码：显示快递的信息和在哪个柜子中，从柜子中移除这个快递

注意：后续扩展真的会引入短信
 

## 快递管理系统分析

模块分析
1. V 视图展示（欢迎，菜单，子菜单）
2. M /Service/ DAO 数据存取（快递数据） 此题中采用存在内存里的方式，没有涉及到数据库
3. C 调度逻辑（根据视图接收到的用户输入内容，调度数据存取）

### 待优化的地方
其实用户和快递员在主流程中的调度逻辑dClient和uClient可以再抽取出来成为单独的两个对象，其中具体1，2，3，4的case操作可以抽取封装成方法，从而简化Main中的流程
