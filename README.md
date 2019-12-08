计182 2018310763 侯志东
# 一、实验目的
##### 1.分析学生选课系统
##### 2.使用GUI窗体及其组件设计窗体界面
##### 3.完成学生选课过程业务逻辑编程
##### 4.基于文件保存并读取数据
##### 5.处理异常
# 二、实验要求
### 一、系统角色分析及类设计
例如：学校有“人员”，分为“教师”和“学生”，教师教授“课程”，学生选择课程。
定义每种角色人员的属性，及其操作方法。
属性示例：	人员（编号、姓名、性别……）
教师（编号、姓名、性别、所授课程、……）
			学生（编号、姓名、性别、所选课程、……）
			课程（编号、课程名称、上课地点、时间、授课教师、……）
以上属性仅为示例，同学们可以自行扩展。

### 二、要求:
##### 1、设计GUI窗体，支持学生注册、课程新加、学生选课、学生退课、打印学生选课列表等操作。
##### 2、基于事件模型对业务逻辑编程，实现在界面上支持上述操作。
##### 3、针对操作过程中可能会出现的各种异常，做异常处理
##### 4、基于输入/输出编程，支持学生、课程、教师等数据的读写操作。
##### 5、基于Github.com提交实验，包括实验SRC源文件夹程序、README.MD实验报告文档。

# 三、实验过程
  1.建立新的GUI
  2.编写文件的写入和读取程序
  3.将写入和读取与GUI结合在一起
  4.输入选课、开课、学生信息写入文件中
# 四、流程图
![](https://github.com/houzhidong/shiyan5/blob/master/%E6%B5%81%E7%A8%8B%E5%9B%BE.jpg)
# 五、核心代码
~~~
 1、ActionListener{ static Xk xk;
	Container c;
	JLabel label1;JLabel label2;JLabel label3;JLabel label4,label5;JLabel label6;
	JLabel label7;JLabel label8;JLabel label9;JLabel label10,label11;JLabel label12;JLabel label13;
	JButton button1,button2;
	JButton button3,button4;
	TextArea ta1,ta2;
	JTextField t1,t2,t3,t4,t5,t6,t7,t8,t9,t10;
	CheckboxGroup cg;
	JCheckBox c1,c2,c3,c4;//建立GUI窗口	
 2、try {
	    	File name1 = new File("D:\\JAVA" + File.separator + "java选课系统.txt");//写入文件
	    	 FileInputStream in=new FileInputStream(name1);
	    	 byte[] buffer=new byte[2048];
	    	 in.read(buffer);
	    	 in.close();
	    	 str=new String(buffer);
	    }
	    
 3、if(e.getSource()==button1) //如果按下第一个按钮
			{ta1.append("姓名："+t1.getText()+"\n"+
			"学号："+t2.getText()+"\n"+"性别："
			+cg.getSelectedCheckbox().getLabel()+
			"\n");
		byte[] se= new byte[4096];
		
		StringBuffer st= new StringBuffer();
			if(c1.isSelected() && e.getSource()==button1)
				{ta1.append( "课程：" + c1.getLabel()+" "+p.toString()+"\n");
				students = new Students(t1.getText(),t2.getText(),cg.getSelectedCheckbox().getLabel(),p);
				StringBuffer s1=new StringBuffer();
				s1.append(students);
				s1.append(p);
				st.append(s1);
			}
			
			
			if(c2.isSelected() && e.getSource()==button1) {
				ta1.append( "课程：" + c2.getLabel()+" "+q.toString()+"\n");
				students = new Students(t1.getText(),t2.getText(),cg.getSelectedCheckbox().getLabel(),q);
				StringBuffer s2=new StringBuffer();
				
				s2.append(q);
				st.append(s2);
			}
			if(c3.isSelected() && e.getSource()==button1) {
				ta1.append( "课程：" + c3.getLabel()+" "+r.toString()+"\n");
				students = new Students(t1.getText(),t2.getText(),cg.getSelectedCheckbox().getLabel(),r);
				StringBuffer s3=new StringBuffer();
				
				s3.append(r);
				st.append(s3);
			}
			if(c4.isSelected() && e.getSource()==button1) {
				ta1.append( "课程：" + c4.getLabel()+" "+s.toString()+"\n");
				students = new Students(t1.getText(),t2.getText(),cg.getSelectedCheckbox().getLabel(),s);
				StringBuffer s4=new StringBuffer();
					
				s4.append(s);
				st.append(s4);
			}	
		try {
				FileWriter fw=new FileWriter("D:\\JAVA\\课程信息.txt");
				fw.write(st.toString());
				fw.close();
			} 
				catch (IOException n) 
					{
					n.printStackTrace();
					}
		    }
			ta1.append("\n");
			if(e.getSource()==button2){
					System.exit(0);
			}
			if(e.getSource()==button4){
			System.exit(0);
		    }
		    if(e.getSource()==button3) {
			ta2.append("教师姓名："+t3.getText()+"\n"+
			"课程："+t4.getText()+"\n"+"上课地点："+t6.getText()
			+"\n"+"\n"+"编号："+t9.getText()
			+"\n"+"学分："+t10.getText()+"\n");
			StringBuffer t=new StringBuffer("教师姓名："+t3.getText()+"\n"+
					"课程："+t4.getText()+"\n"+"上课地点："+t6.getText()
					+"\n"+"\n"+"编号："+t9.getText()
					+"\n"+"学分："+t10.getText());//输入的信息写入文件中
~~~
# 六、实验结果
![](https://github.com/houzhidong/shiyan5/blob/master/yuxing.png)

![](https://github.com/houzhidong/shiyan5/blob/master/1.png)

![](https://github.com/houzhidong/shiyan5/blob/master/2.png)

![](https://github.com/houzhidong/shiyan5/blob/master/3.png)
# 七、实验感想
  这次实验综合性较强，是将之前的实验内容结合在一起，做完这次实验后我更加深入的了解了GUI和文件的输入输出。Java编程需要有一定的逻辑，也需要对很多的函数熟练运用，这就需要自己在百度上搜索查找和运用，学会了GUI的容器、组件等。也能更加熟练地使用GitHub以及README的排版了，对Java有了更深的理解。希望以后还能更加深入的了解Java。

