一个简单的分段控制器，使用时只需将SegmentView文件夹拖入项目中，在需要使用的VC中导入#import "MainView.h"。
具体使用demo如下：
- (void)createVc {
    FirstController   *firstVc  = [[FirstController alloc] init];
    
    SecondController  *secondVc = [[SecondController alloc] init];
    
    ThirdController   *ThirdVc  = [[ThirdController alloc] init];
    
    [self addChildViewController:firstVc];
    
    [self addChildViewController:secondVc];
    
    [self addChildViewController:ThirdVc];
    
    self.viewControllers        = [NSArray arrayWithObjects:firstVc,secondVc,ThirdVc,nil];
    
    MainView *main = [[MainView alloc] init];
    
    [self.view addSubview:main];
    
    main.frame = CGRectMake(0, 64,self.view.frame.size.width, self.view.frame.size.height-64);
    
    //设置菜单view 的高度
    
    main.btnViewHeight = 30;
    
    //设置按钮下划线高度
    
    main.btnLineHeight = 2;
    
    //设置按钮字体大小
    main.btnFont       = 17;
    
    main.viewControllers = self.viewControllers;
    
    NSArray *array  = @[@"第一页",@"第二页",@"第三页"];
    
    main.titleArray = array;
    
}


按照createVc 这个方法里面的进行设置即可。。

