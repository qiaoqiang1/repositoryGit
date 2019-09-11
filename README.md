
# Source File
> ## *This file contains:*  
  >> * *DG822.h、DM3058E.h、DG822_visa.h*  
  >> * *DG822.cpp、DM3058E.cpp、DG822_visa.cpp ...*  
   
> ### *DG822.h*   
 >> *  *void **Out\_Bas\_Wave** (int ch, char * wave, double fre, double Vpp, double Vdc, double phase)*     
 >> *  *void **Out\_Ran\_Wave**(int ch, double fre, double Vpp, double Vdc, double phase)*   
 >> * *void **Out\_Pulse**(int ch, double fre, double Vpp, double Vdc, double phase)*    
 >> * *void **set\_Puls_Dcyc**(int ch, double duty)*    
 >> * *void **set\_PWM\_DCYCle**(int ch, double duty)*  
 >> * *void **set\_PWM\_Pulwid**(int ch, double duty)*  
 >> * *void **set\_PWM\_Wave**(int ch, char * wave)*  
 >> * *void **set\_PWM\_Freq**(int ch, double fre)*    
 >> *	*void **set\_PWM\_Sig\_Sou**(int ch, char * flag)*  
 >> *	*void **Open\_PWM**(int ch)*  
 >> *	*void **Close\_PWM**(int ch)*  

> ### *DM3085E.h*
 >> * *void **OpenMeasure**(const char * sig,const char * mod)*    	
 >> * *void **setRate**(const char * sig, const char * mod,const char * rate)*  
 >> * *void **InqInfo**(const char * sig, const char * mod)*  
> ### *DG822\_visa.h*

	DG822_visa(QWidget *parent = Q_NULLPTR);
	~DG822_visa();
	void Init();		//界面初始化
	bool FileInit();	//文件操作初始化
	void progressBarInit();		//进度条初始化
	void Delay_MSec(int sec);	//延时sec ms
	void CreatCSV();			//导出csv表格
	double DataProcess(QString string);	  //科学计数法转一般计数
	void setupRealtimeDataDemo(QCustomPlot *customPlot);	//设置qcustomplot画图属性，实时
	signals:
		void TestSignal();	//测试信号  触发方式：点击stratButon，
	signals:
		void realDataSignal();	//数据处理完毕信号 触发方式：DataProcess（）数据处理完毕
	signals:
		void DevicenofSignal();//设备未检测到信号 触发方式：设备未检测到

	private slots:
		void Up_DutyBoxSolt();	// 
		void StratButtonSolt();	//StratButton槽函数
		void CloseButtonSolt();//CloseButton槽函数
		void CopyCHnButtonSlot();//CopyCHnButton槽函数
		void SetCHnButtonSlot();//SetCHnButton槽函数
		void TestSlot();		//测试槽函数
		void realtimeDataSlot();//添加实时数据槽
# *Links*  
 
* QT 5.9.4:  *[Download](http://download.qt.io/archive/qt/5.9/5.9.4/)*
* QCustomPlot 2:  *[Download](https://www.qcustomplot.com/index.php/download)*
* Wiki:  *[View](http://192.168.123.39:3300/Vogue/wud/wiki)*  


 ![zhanshi](https://github.com/qiaoqiang1/hello-world/blob/master/images/create-octocat.png)
