# PagerTopTabIndicator
根据PagerSlidingTabStrip进行部分修改,添加属性,实现设置tab的字体颜色
## 具体实现方式根据PagerSlidingTabStrip修改,添加
# 使用方式:
 Step 1
 Add it in your root build.gradle at the end of repositories:
## 
    allprojects {
		repositories {
			...
			maven { url 'https://jitpack.io' }
		}
	}
 Step 2. Add the dependency
## 
	dependencies {
	        compile 'com.github.Simonhy:PagerTopTabIndicator:v1.0'
	}
## 代码中使用

In your onCreate method (or onCreateView for a fragment), bind the widget to the ViewPager.

// Initialize the ViewPager and set an adapter
ViewPager pager = (ViewPager) findViewById(R.id.pager);
pager.setAdapter(new TestAdapter(getSupportFragmentManager()));

## // Bind the tabs to the ViewPager
		PagerSlidingTabStrip tabs = (PagerSlidingTabStrip) findViewById(R.id.tabs);
		tabs.setViewPager(pager);
(Optional) If you use an OnPageChangeListener with your view pager you should set it in the widget rather than on the pager directly.

## // continued from above
	tabs.setOnPageChangeListener(mPageChangeListener);
## Customization

 ### To not just look like another Play Store styled app, go and adjust these values to match your brand:

	pstsIndicatorColor Color of the sliding indicator
	pstsUnderlineColor Color of the full-width line on the bottom of the view
	pstsDividerColor Color of the dividers between tabs
	pstsIndicatorHeightHeight of the sliding indicator
	pstsUnderlineHeight Height of the full-width line on the bottom of the view
	pstsDividerPadding Top and bottom padding of the dividers
	pstsTabPaddingLeftRight Left and right padding of each tab
	pstsScrollOffset Scroll offset of the selected tab
	pstsTabBackground Background drawable of each tab, should be a StateListDrawable
	pstsShouldExpand If set to true, each tab is given the same weight, default false
	pstsTextAllCaps If true, all tab titles will be upper case, default true
	hyTabTextSize  
	hySelectTextColor
        hySelectedTabTextSize
        hySelectedTabTextColor
