# VerticalRollingTextView
竖直方向无限循环滚动显示单行文本的控件

**非常轻量级,直接继承View实现,使用Paint绘制文本,不依赖任何第三方!!!**

![image](https://github.com/shubowen/VerticalRollingTextView/blob/master/app/image.gif)

**使用方法:**

1.现在布局文件中声明

    <LinearLayout
            android:layout_width="match_parent"
            android:layout_height="50dp"
            android:background="@android:color/white"
            android:gravity="center_vertical">
    
            <ImageView
                android:layout_width="wrap_content"
                android:layout_height="wrap_content"
                android:layout_marginLeft="15dp"
                android:src="@mipmap/gd_xiaoxi"/>
    
            <com.xiaosu.VerticalRollingTextView
                android:id="@+id/verticalRollingView"
                android:layout_width="match_parent"
                android:layout_height="match_parent"
                android:layout_marginLeft="10dp"/>
    
    </LinearLayout>
    
2.代码中设置数据集:

    mVerticalRollingView.setDataSetAdapter(new DataSetAdapter<String>(Arrays.asList(mStrs)) {
    
                @Override
                protected String text(String s) {
                    return s;
                }
            });
    
3.开始滚动:

    mVerticalRollingView.run();
    
4.暂停:

    mVerticalRollingView.stop();

5.设置点击监听:

    mVerticalRollingView.setOnItemClickListener(this);

6.点击回调
    
    public void onItemClick(VerticalRollingTextView view, int index) {
        //index是当前条目的角标
    }

7.可以设置文字的大小:

    android:textSize="16dp"
    
8.可以设置文字的颜色:

    android:textColor="#FF0000"

    
