
## インストール

* [ここ](https://github.com/dotstudio/Grove_LED_Bar_WioLTE)からzipファイルをDL
* スケッチ -> ライブラリをインクルード -> .zip形式のライブラリをインストール
* DLしたzipファイルを選択

## 使い方

サンプルコードの`#include <Grove_LED_Bar.h>`になってる箇所を`#include <Grove_LED_Bar_WioLTE.h>`に変更すると動きます。

```
#include <WioCellLibforArduino.h>
#include <Grove_LED_Bar_WioLTE.h> //変更点

Grove_LED_Bar bar(WIO_D39, WIO_D38, 0);  // Clock pin, Data pin, Orientation

void setup(){
  bar.begin();
}

void loop(){
  for (int i = 0; i <= 10; i++){
    bar.setLevel(i);
    delay(100);
  }
}
```

このサンプルだと↓のGIFのような挙動をしてくれます。

## 以下はフォーク元のREADME

Grove LED Bar
-------------------------------------------------------------
![image](Grove_LED_Bar.gif)

[Grove LED Bar v2.0](https://www.seeedstudio.com/Grove-LED-Bar-v2.0-p-2474.html)

Grove LED Bar is comprised of a 10 segment LED gauge bar and an MY9221 LED driver.
It can be used as a indicator for remaining battery life, voltage, water level, music volume or other values that require a gradient display.
There are 10 discrete LED bars in the LED bar graph: one red, one yellow, one light green, and the rest green.


For more information, please refer to the [wiki](http://wiki.seeedstudio.com/Grove-LED_Bar/).


----

This software is written by Frankie Chu for seeed studio<br>
and is licensed under [The MIT License](http://opensource.org/licenses/mit-license.php). Check License.txt for more information.<br>

Contributing to this software is warmly welcomed. You can do this basically by<br>
[forking](https://help.github.com/articles/fork-a-repo), committing modifications and then [pulling requests](https://help.github.com/articles/using-pull-requests) (follow the links above<br>
for operating guide). Adding change log and your contact into file header is encouraged.<br>
Thanks for your contribution.

Seeed Studio is an open hardware facilitation company based in Shenzhen, China. <br>
Benefiting from local manufacture power and convenient global logistic system, <br>
we integrate resources to serve new era of innovation. Seeed also works with <br>
global distributors and partners to push open hardware movement.<br>


[![Analytics](https://ga-beacon.appspot.com/UA-46589105-3/Grove_LED_Bar)](https://github.com/igrigorik/ga-beacon)
