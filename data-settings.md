# data-settings.xml 接口的使用说明

## 注意：

>**被 `<!-- -->` 括起来的文字是做解释说明之用，不需要修改；**

>**添加工作片、行政村、抽查内容、科室等之后不需要修改数量，设置文件中也没有提供改数量的地方，程序能够自动计算数量；**

## 一、添加工作片
- 添加之前：

```html
<gongZuoPian name="东朱片">
  <village>
    <value>东朱村</value>
    <value>南青口村</value>
    <value>薛乔村</value>
  </village>
</gongZuoPian>
......
```

- 添加之后：

```html
<gongZuoPian name="东朱片">
  <village>
    <value>东朱村</value>
    <value>南青口村</value>
    <value>薛乔村</value>
  </village>
</gongZuoPian>

<gongZuoPian name="新工作片名称">
  <village>
    <value>新工作片下的村庄1</value>
    <value>新工作片下的村庄2</value>
    <value>新工作片下的村庄3</value>
  </village>
</gongZuoPian>
......
```

## 二、修改转盘转动速度

- 修改前：

```html
<!-- 转盘旋转一次所需的时间，单位 s，默认是 6s -->
<rotateTime>6</rotateTime>
```

- 修改后：

```html
<!-- 转盘旋转一次所需的时间，单位 s，默认是 6s -->
<rotateTime>4</rotateTime>
```

>**数值越小，转盘转动越快**

## 三、修改转盘扇形上的文本字体大小

- 修改前：

```html
<!-- 扇形的字体大小，默认值是 16 -->
<fontSize>16</fontSize>
```

- 修改后：

```html
<!-- 扇形的字体大小，默认值是 16 -->
<fontSize>14</fontSize>
```

## 四、修改转盘扇形颜色、字体颜色和转盘中心的指针颜色

- 修改前：

```html
<!-- 插件用到的颜色 -->
<colors>
  <!-- 扇形颜色一 -->
  <value>#e9536a</value>
  <!-- 扇形颜色二 -->
  <value>#fbd7a1</value>
  <!-- 扇形颜色三：当扇形数为奇数时，最后一块扇形的颜色，如：总共有 5 个工作片，则第五个工作片在转盘上的扇形颜色就用 颜色三 填充，这样就能保证不会跟两边的扇形颜色重合 -->
  <value>#df6679</value>
  <!-- 扇形字体颜色 -->
  <value>#000</value>
  <!-- 指针字体颜色 -->
  <value>#fff</value>
  <!-- 指针和边框颜色 -->
  <value>#666</value>
</colors>
```

- 修改后：

```html
<!-- 插件用到的颜色 -->
<colors>
  <!-- 扇形颜色一 -->
  <value>red</value>
  <!-- 扇形颜色二 -->
  <value>blue</value>
  <!-- 扇形颜色三：当扇形数为奇数时，最后一块扇形的颜色，如：总共有 5 个工作片，则第五个工作片在转盘上的扇形颜色就用 颜色三 填充，这样就能保证不会跟两边的扇形颜色重合 -->
  <value>green</value>
  <!-- 扇形字体颜色 -->
  <value>black</value>
  <!-- 指针字体颜色 -->
  <value>pink</value>
  <!-- 指针和边框颜色 -->
  <value>yellow</value>
</colors>
```

>**常用的颜色可以填写英文单词，如：red、black、blue等，不常用的颜色则需要用 16 进制填写，如：#e9536a（暗红色）、#fbd7a1（深红色）等；**

## 五、添加抽查内容

- 添加前：

```html
<value name="村情">
  <link>./Docs/doc1</link>
</value>
<value name="党建基本情况">
  <link>./Docs/doc1</link>
</value>
......
```

- 添加后：

```html
<value name="村情">
  <link>./Docs/doc1</link>
</value>
<value name="党建基本情况">
  <link>./Docs/doc1</link>
</value>
<value name="新的抽查内容">
  <link>此处填入新的抽查内容在本地电脑上的路径</link>
</value>
......
```

>**抽查内容的路径应填入相对路径**

## 六、修改选抽查内容时的跳动速度

- 修改前：

```html
<!-- 随机跳动的速度，默认为 70(ms); 1s = 1000ms -->
<rollSpeed>70</rollSpeed>
```

- 修改后：

```html
<!-- 随机跳动的速度，默认为 70(ms); 1s = 1000ms -->
<rollSpeed>200</rollSpeed>
```

>**数值越小，跳动得越快**

## 七、修改选抽查内容时的随机跳动次数

- 修改前：

```html
<!-- 从点击开始到停止随机跳动的次数，默认为 30 次 -->
<rollTime>30</rollTime>
```

- 修改后：

```html
<!-- 从点击开始到停止随机跳动的次数，默认为 30 次 -->
<rollTime>5</rollTime>
```

>**数值越小，越快停止跳动**

## 八、添加科室

- 添加前：

```html
<name>党政综合办</name>
<name>组织线</name>
......
```

- 添加后：

```html
<name>党政综合办</name>
<name>组织线</name>
<name>新的科室名称</name>
......
```