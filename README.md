计182 2018310763 侯志东
# 一、实验目的
##### 1.分析学生选课系统
##### 2.使用GUI窗体及其组件设计窗体界面
##### 3.完成学生选课过程业务逻辑编程
##### 4.基于文件保存并读取数据
##### 5.处理异常
# 二、实验要求
## 一、系统角色分析及类设计
例如：学校有“人员”，分为“教师”和“学生”，教师教授“课程”，学生选择课程。
定义每种角色人员的属性，及其操作方法。
属性示例：	人员（编号、姓名、性别……）
教师（编号、姓名、性别、所授课程、……）
			学生（编号、姓名、性别、所选课程、……）
			课程（编号、课程名称、上课地点、时间、授课教师、……）
以上属性仅为示例，同学们可以自行扩展。

## 二、要求:
##### 1、设计GUI窗体，支持学生注册、课程新加、学生选课、学生退课、打印学生选课列表等操作。
##### 2、基于事件模型对业务逻辑编程，实现在界面上支持上述操作。
##### 3、针对操作过程中可能会出现的各种异常，做异常处理
##### 4、基于输入/输出编程，支持学生、课程、教师等数据的读写操作。
##### 5、基于Github.com提交实验，包括实验SRC源文件夹程序、README.MD实验报告文档。

# 三、实验过程
   建立新的类GUI，通过调用之前的Xk、Students和Peoples的类进行对GUI的编辑。运用各种窗口组件，来建立可行的GUI窗口。先建立各个不同的组件，给各个不同的组件进行赋值。再在容器中引用他们。最后在文本框中输出要输出的内容。新建课程文件来储存课程的信息，在用户选择课程后再从文件中提取相应的内容，在写到新建的另一个文件。开课将用户所输入的信息储存到文件中
# 四、流程图
![](https://github.com/houzhidong/shiyan5/blob/master/%E6%B5%81%E7%A8%8B%E5%9B%BE.jpg)
# 五、核心代码
ActionListener{ static Xk xk;
	Container c;
	JLabel label1;JLabel label2;JLabel label3;JLabel label4,label5;JLabel label6;
	JLabel label7;JLabel label8;JLabel label9;JLabel label10,label11;JLabel label12;JLabel label13;
	JButton button1,button2;
	JButton button3,button4;
	TextArea ta1,ta2;
	JTextField t1,t2,t3,t4,t5,t6,t7,t8,t9,t10;
	CheckboxGroup cg;
	JCheckBox c1,c2,c3,c4;//建立GUI窗口
	

 try {
	    	File name1 = new File("D:\\JAVA" + File.separator + "java选课系统.txt");//写入文件
	    	 FileInputStream in=new FileInputStream(name1);
	    	 byte[] buffer=new byte[2048];
	    	 in.read(buffer);
	    	 in.close();
	    	 str=new String(buffer);
	    }
# 六、实验结果
![](https://github.com/houzhidong/shiyan5/blob/master/yuxing.png)

![](https://github.com/houzhidong/shiyan5/blob/master/1.png)

![](https://github.com/houzhidong/shiyan5/blob/master/2.png)

![](https://github.com/houzhidong/shiyan5/blob/master/3.png)
# 七、实验感想




