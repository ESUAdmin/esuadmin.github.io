## 转换比率
### 24-bit
|程式|浮点到定点（正）|浮点到定点（负）|定点到浮点（正）|定点到浮点（负）|
|-|-|-|-|-|
|foobar2000|8388608|8388608|8388608|8388608|
|FFmpeg|8388608|8388608|8388608|8388608|
|Audition|8388608|8388608|8388608|8388608|

### 16-bit
|程式|浮点到定点（正）|浮点到定点（负）|定点到浮点（正）|定点到浮点（负）|
|-|-|-|-|-|
|foobar2000|32768|32768|32768|32768|
|FFmpeg|32768|32768|32768|32768|
|Audition|32768|32768|32768|32768|

## 定点舍入规则
### 24-bit
|程式|0|-0|0.25|-0.25|0.5|-0.5|0.75|-0.75|1|-1|1.5|-1.5|判定|
|-|-|-|-|-|-|-|-|-|-|-|-|-|-|
|foobar2000|0|0|0|0|0|0|1|-1|1|-1|2|-2|四舍六入五成双|
|FFmpeg|0|0|0|-1|0|-1|0|-1|1|-1|1|-2|地板|
|Audition|0|0|0|0|1|0|1|-1|1|-1|2|-1|JS 式舍入|

### 16-bit
|程式|0|-0|0.25|-0.25|0.5|-0.5|0.75|-0.75|1|-1|1.5|-1.5|判定|
|-|-|-|-|-|-|-|-|-|-|-|-|-|-|
|foobar2000|0|0|0|0|0|0|1|-1|1|-1|2|-2|四舍六入五成双|
|FFmpeg|0|0|0|0|0|0|1|-1|1|-1|2|-2|四舍六入五成双|
|Audition|0|0|0|0|1|0|1|-1|1|-1|2|-1|JS 式舍入|
