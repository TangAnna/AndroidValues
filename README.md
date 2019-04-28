# AndroidValues
Android 使用values进行屏幕适配 生成values文件<br>

使用values文件进行适配时，主要的问题就是values文件不全时会导致页面有差别，所以默认的lay_x、lay_y使用的是1px=0.5dp
的关系生成的，就算没有对应的values文件也不会有太大的变形;<br>
AndroidDimensUtil类中要根据UI设计的尺寸进行修改标准尺寸值:<br>
```
    /**
             * 基准宽度和高度(通常设置成UI图的分辨率的高度和宽度)
             */
            private static final int baseHeight = 1334;
            private static final int baseWidth = 750;
```
现在大多数的UI标注图是按照iOS的尺寸做的，所以是750*1334;<br>
注：有些手机的尺寸和实际代码获得的尺寸是不一样的，可以自行在AndroidDimensUtil中添加你想要的规格;


AndroidDimensUtil运行方式：放在AndroidStudio中右键选择 Run 'AndroidDimensUtil....main()'就可以了;
