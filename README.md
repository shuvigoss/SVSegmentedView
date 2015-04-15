# SVSegmentedView
ios Segmented 高仿网易新闻

# storyBoard:
<pre>
@property (strong, nonatomic) IBOutlet SVSegmentedView *svSegmentedView;

- (void)viewDidLoad {
  [super viewDidLoad];
  _svSegmentedView.titles = @[@"头条", @"娱乐", @"体育", @"北京", @"科技", @"军事", @"图片", @"跟帖", @"段子", @"汽车", @"房产", @"岛国娱乐..."];
  _svSegmentedView.defaultFont = [UIFont fontWithName:SV_SEGMENTEDVIEW_DEFAULT_FONT_NAME size:14];
  _svSegmentedView.minTitleMargin = 15;
  _svSegmentedView.selectedFontSize = 17;
//  _svSegmentedView.horizontalMargin = 10;
  _svSegmentedView.delegate = self;
  _svSegmentedView.duplicateNotification = YES;
} 
//返回值决定是否切换segmented
- (BOOL)segmentedWillChange:(NSInteger)index oldIndex:(NSInteger)oldIndex{
  return YES;
}

- (void)segmentedDidChange:(NSInteger)index{
  NSLog(@"%i", index);
}
</pre>

# 非storyBoard

直接当成一个view来使用， init frame 即可
