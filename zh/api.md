# API

## Line

`Line` 是判定线。

参数：
+ x: 即第一个参数，表示判定线中心点横坐标
+ y: 即第二个参数，表示判定线中心点纵坐标
+ angle: 即第三个参数，可省略，表示判定线旋转角度
+ width: 即第四个参数，可省略，表示判定线宽度

## Click, Drag, Flick

这三种音符只有材质不同，其他方面都一样。

参数：
+ sec: 即第一个参数，表示音符触摸时间
+ pos: 即第二个参数，表示音符在判定线上的位置。注意是相对于判定线中心的位置
+ speed：即第三个参数，表示音符下落速度
+ show_sec: 即第四个参数，可省略，表示音符出现时间，如果不填或为 `None` 则表示进入视野范围后自动显示
+ line: 即第五个参数，可省略，表示要绑定的判定线。如果不填或为 `None` 则表示使用自动绑定

## Hold

相对于 [其他三种音符](#click-drag-flick)，多了时长这一参数。

参数：
+ sec: 即第一个参数，表示音符触摸时间
+ pos: 即第二个参数，表示音符在判定线上的位置。注意是相对于判定线中心的位置
+ speed：即第三个参数，表示音符下落速度
+ duration: 即第四个参数，表示持续时长
+ show_sec: 即第五个参数，可省略，表示音符出现时间，如果不填或为 `None` 则表示进入视野范围后自动显示
+ line: 即第六个参数，可省略，表示要绑定的判定线。如果不填或为 `None` 则表示使用自动绑定

## Offset

`Offset` 的作用是：把所有它之后事件的时间（包括：音符触摸时间、音符动画效果触发时间、判定线动画效果触发时间、`Offset`），全部推迟若干个时间单位。

## Multiplier

`Multiplier` 的作用是：把在它控制范围内的时间轴整体缩放若干倍；或者说，把在它控制范围内的所有“时间”（包括：音符触摸时间、`Hold` 类型音符的持续时间、音符动画效果触发时间、判定线动画效果触发时间、`Offset`），全部乘以某个给定的数。

## preview

preview 用来预览谱面。

参数：
+ name: 即第一个参数，可省略，默认为 `'test'`，表示曲名，将会显示在左下角
+ diff: 即第二个参数，可省略，默认为 `'EZ Lv.0'`，表示难度，将会显示在右下角
+ music: 即第三个参数，可省略，表示音乐文件，如果不填或为 `None` 则表示不播放音乐
+ background: 即第四个参数，可省略，表示背景文件，如果不填或为 `None` 则表示不设置背景
+ height: 可省略，默认为 `600`，表示窗口高度，**不影响谱面区域大小**
+ width: 可省略，默认为 `800`，表示窗口宽度，**不影响谱面区域大小**
+ **size: 可省略，默认为 `600`，表示谱面放大比例**
+ opacity: 可省略，默认为 `127`，表示背景图片不透明度
+ font_name: 可省略，默认为 `['Electrolize']`（该字体已内置，无需安装），表示使用的字体列表
