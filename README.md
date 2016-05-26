DBCalendarView
========
>由于项目需要用到日历控件，在github中搜索了一些相关的项目，最后决定使用lichao315同学的这个。
>
>再次感谢lichao315
>
>修改及增加方法详见注释。

原链接： https://github.com/lichao315/Calendar 

这是一个符合中国人使用习惯的Android上自定义日历控件。

该日历集成公历农历显示、节假日和二十四节气的显示。代码小巧玲珑，易于项目整合。提供农历算法、闰年月算法。
日历本身为动态代码生成的6*7的GridView，结合ViewFlipper完成日历的滑动切换功能。

------------

新增方法：
------------

1. setOnlyDay(boolean)

        true  - 仅显示日期(公历+阴历)   
        
        false - 显示纪念日、节假日 
    
    ```
       
        //农历部分节假日
        
        final static String[] lunarHoliday = new String[] { "0101 春节", "0115 元宵", "0505 端午", "0707 情人", "0715 中元", "0815 中秋", "0909 重阳", "1208 腊八", "1224 小年", "0100 除夕" };
       
        // 公历部分节假日
        
        final static String[] solarHoliday = new String[] { //
        "0101 元旦", "0214 情人", "0308 妇女", "0312 植树", "0315 消费者权益日", "0401 愚人", "0501 劳动", "0504 青年", //
                "0512 护士", "0601 儿童", "0701 建党", "0801 建军", "0808 父亲", "0909 毛泽东逝世纪念", "0910 教师", "0928 孔子诞辰",//
                "1001 国庆", "1006 老人", "1024 联合国日", "1112 孙中山诞辰纪念", "1220 澳门回归纪念", "1225 圣诞", "1226 毛泽东诞辰纪念" };
                
    ```

2. setOnlyMonth(boolean)
    
        true - 仅显示当前月份日历
    
        false - 上月、下月日历均显示
