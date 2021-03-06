#### 全国新型肺炎疫情实时动态获取渠道：

- [ ] 丁香医生： [https://ncov.dxy.cn/ncovh5/view/pneumonia]( https://ncov.dxy.cn/ncovh5/view/pneumonia )

- [ ] 百度：[ https://voice.baidu.com/act/newpneumonia/newpneumonia ]( https://voice.baidu.com/act/newpneumonia/newpneumonia )

- [ ] 网易：[http://news.163.com/special/epidemic](http://news.163.com/special/epidemic)

- [ ] 新浪： [ https://news.sina.cn/zt_d/yiqing0121 ]( https://news.sina.cn/zt_d/yiqing0121 )

- [ ] 腾讯：[https://news.qq.com//zt2020/page/feiyan.htm](https://news.qq.com//zt2020/page/feiyan.htm)

- [ ] 阿里：[ https://alihealth.taobao.com/medicalhealth/influenzamap ]( https://alihealth.taobao.com/medicalhealth/influenzamap )

- [ ] 微医： [ https://promo.guahao.com/topic/pneumonia ]( https://promo.guahao.com/topic/pneumonia )

- [ ] 知乎： [ https://www.zhihu.com/special/19681091 ]( https://www.zhihu.com/special/19681091 )

- [ ] 夸克： [ https://broccoli.uc.cn/apps/pneumonia/routes/index ]( https://broccoli.uc.cn/apps/pneumonia/routes/index )

- [ ] 搜狗： [ http://sa.sogou.com/new-weball/page/sgs/epidemic ]( http://sa.sogou.com/new-weball/page/sgs/epidemic )

- [ ] 凤凰： [ https://news.ifeng.com/c/special/7tPlDSzDgVk ]( https://news.ifeng.com/c/special/7tPlDSzDgVk )


<hr/>


###  `virus.py`爬取的丁香园上的信息(请使用version 2, 以避免不必要的问题)

  当时爬取的两个主要页面 ：

- [主页面](1.html) 
- [加载出的js](./3.js)  url 变成 3.js (version 2 中使用加载出的[json文件](case_timeline_list.json))

<p style='font-weight:bold''>
注意：
</p>

- ~~目前`get_broadcast()`函数不能够正确获取实时的信息，目前可以直接使用网页加载出来的`json`文件，目前网页链接为 [https://file1.dxycdn.com/2020/0127/794/3393185296027391740-115.json](https://file1.dxycdn.com/2020/0127/794/3393185296027391740-115.json), 可自行在`F12`之后`network`中获取~~  <br>(version 2 中已解决)



<hr>

### `virus_sina.py`爬取新浪微博上的信息

- 主要使用的是网页加载出的`json`文件，比丁香医生网上要简单



<hr>



爬取出来的部分数据：

<hr/>
<table border="1" style="border-collapse:collapse">
<tr><th>provinceName</th><th>provinceShortName</th><th>confirmedCount</th><th>suspectedCount</th><th>curedCount</th><th>deadCount</th><th>comment</th></tr>
<tr><td>湖北省</td><td>湖北</td><td>549</td><td>0</td><td>31</td><td>24</td><td></td></tr>
<tr><td>广东省</td><td>广东</td><td>53</td><td>0</td><td>2</td><td>0</td><td></td></tr>
<tr><td>浙江省</td><td>浙江</td><td>43</td><td>0</td><td>1</td><td>0</td><td></td></tr>
<tr><td>北京市</td><td>北京</td><td>36</td><td>0</td><td>1</td><td>0</td><td></td></tr>
<tr><td>重庆市</td><td>重庆</td><td>27</td><td>0</td><td>0</td><td>0</td><td></td></tr>
<tr><td>湖南省</td><td>湖南</td><td>24</td><td>0</td><td>0</td><td>0</td><td></td></tr>
<tr><td>上海市</td><td>上海</td><td>20</td><td>0</td><td>1</td><td>0</td><td></td></tr>
<tr><td>四川省</td><td>四川</td><td>15</td><td>0</td><td>0</td><td>0</td><td></td></tr>
<tr><td>山东省</td><td>山东</td><td>15</td><td>0</td><td>0</td><td>0</td><td></td></tr>
<tr><td>安徽省</td><td>安徽</td><td>15</td><td>0</td><td>0</td><td>0</td><td></td></tr>
<tr><td>广西壮族自治区</td><td>广西</td><td>13</td><td>0</td><td>0</td><td>0</td><td></td></tr>
<tr><td>福建省</td><td>福建</td><td>10</td><td>2</td><td>0</td><td>0</td><td>福建地区新增疑似 2 例（漳州 1 例；三明 1 例）</td></tr>
<tr><td>河南省</td><td>河南</td><td>9</td><td>0</td><td>0</td><td>0</td><td></td></tr>
<tr><td>江苏省</td><td>江苏</td><td>9</td><td>0</td><td>0</td><td>0</td><td></td></tr>
<tr><td>海南省</td><td>海南</td><td>8</td><td>0</td><td>0</td><td>0</td><td></td></tr>
<tr><td>天津市</td><td>天津</td><td>8</td><td>0</td><td>0</td><td>0</td><td></td></tr>
<tr><td>江西省</td><td>江西</td><td>7</td><td>0</td><td>0</td><td>0</td><td></td></tr>
<tr><td>陕西省</td><td>陕西</td><td>5</td><td>0</td><td>0</td><td>0</td><td></td></tr>
<tr><td>黑龙江省</td><td>黑龙江</td><td>4</td><td>0</td><td>0</td><td>1</td><td></td></tr>
<tr><td>辽宁省</td><td>辽宁</td><td>4</td><td>0</td><td>0</td><td>0</td><td></td></tr>
<tr><td>贵州省</td><td>贵州</td><td>3</td><td>0</td><td>0</td><td>0</td><td></td></tr>
<tr><td>吉林省</td><td>吉林</td><td>3</td><td>0</td><td>0</td><td>0</td><td></td></tr>
<tr><td>云南省</td><td>云南</td><td>2</td><td>0</td><td>0</td><td>0</td><td></td></tr>
<tr><td>宁夏回族自治区</td><td>宁夏</td><td>2</td><td>0</td><td>0</td><td>0</td><td></td></tr>
<tr><td>香港</td><td>香港</td><td>2</td><td>0</td><td>0</td><td>0</td><td></td></tr>
<tr><td>澳门</td><td>澳门</td><td>2</td><td>0</td><td>0</td><td>0</td><td></td></tr>
<tr><td>河北省</td><td>河北</td><td>2</td><td>0</td><td>0</td><td>1</td><td></td></tr>
<tr><td>甘肃省</td><td>甘肃</td><td>2</td><td>0</td><td>0</td><td>0</td><td></td></tr>
<tr><td>新疆维吾尔自治区</td><td>新疆</td><td>2</td><td>0</td><td>0</td><td>0</td><td></td></tr>
<tr><td>台湾</td><td>台湾</td><td>1</td><td>0</td><td>0</td><td>0</td><td></td></tr>
<tr><td>山西省</td><td>山西</td><td>1</td><td>0</td><td>0</td><td>0</td><td></td></tr>
<tr><td>内蒙古自治区</td><td>内蒙古</td><td>1</td><td>0</td><td>0</td><td>0</td><td></td></tr>
<tr><td>青海省</td><td>青海</td><td>0</td><td>1</td><td>0</td><td>0</td><td>西宁新增疑似 1 例</td></tr></table>

<hr/>
<table border="1" style="border-collapse:collapse">
<tr><th>provinceShortName</th><th>cityName</th><th>confirmedCount</th><th>suspectedCount</th><th>curedCount</th><th>deadCount</th></tr>
<tr><td>湖北</td><td>武汉</td><td>495</td><td>0</td><td>31</td><td>23</td></tr>
<tr><td>湖北</td><td>孝感</td><td>22</td><td>0</td><td>0</td><td>0</td></tr>
<tr><td>湖北</td><td>黄冈</td><td>12</td><td>0</td><td>0</td><td>0</td></tr>
<tr><td>湖北</td><td>荆州</td><td>8</td><td>0</td><td>0</td><td>0</td></tr>
<tr><td>湖北</td><td>荆门</td><td>8</td><td>0</td><td>0</td><td>0</td></tr>
<tr><td>湖北</td><td>仙桃</td><td>2</td><td>0</td><td>0</td><td>0</td></tr>
<tr><td>湖北</td><td>宜昌</td><td>1</td><td>0</td><td>0</td><td>1</td></tr>
<tr><td>湖北</td><td>十堰</td><td>1</td><td>0</td><td>0</td><td>0</td></tr>
<tr><td>广东</td><td>深圳</td><td>15</td><td>0</td><td>2</td><td>0</td></tr>
<tr><td>广东</td><td>珠海</td><td>8</td><td>0</td><td>0</td><td>0</td></tr>
<tr><td>广东</td><td>佛山</td><td>7</td><td>0</td><td>0</td><td>0</td></tr>
<tr><td>广东</td><td>广州</td><td>7</td><td>0</td><td>0</td><td>0</td></tr>
<tr><td>广东</td><td>惠州</td><td>5</td><td>0</td><td>0</td><td>0</td></tr>
<tr><td>广东</td><td>韶关</td><td>3</td><td>0</td><td>0</td><td>0</td></tr>
<tr><td>广东</td><td>阳江</td><td>3</td><td>0</td><td>0</td><td>0</td></tr>
<tr><td>广东</td><td>湛江</td><td>2</td><td>0</td><td>0</td><td>0</td></tr>
<tr><td>广东</td><td>中山</td><td>2</td><td>0</td><td>0</td><td>0</td></tr>
<tr><td>广东</td><td>肇庆</td><td>1</td><td>0</td><td>0</td><td>0</td></tr>
<tr><td>广东</td><td>清远</td><td>1</td><td>0</td><td>0</td><td>0</td></tr>
<tr><td>浙江</td><td>台州</td><td>18</td><td>0</td><td>0</td><td>0</td></tr>
<tr><td>浙江</td><td>杭州</td><td>6</td><td>0</td><td>0</td><td>0</td></tr>
<tr><td>浙江</td><td>温州</td><td>6</td><td>0</td><td>1</td><td>0</td></tr>
<tr><td>浙江</td><td>宁波</td><td>5</td><td>0</td><td>0</td><td>0</td></tr>
<tr><td>浙江</td><td>嘉兴</td><td>3</td><td>0</td><td>0</td><td>0</td></tr>
<tr><td>浙江</td><td>衢州</td><td>2</td><td>0</td><td>0</td><td>0</td></tr>
<tr><td>浙江</td><td>舟山</td><td>1</td><td>0</td><td>0</td><td>0</td></tr>
<tr><td>浙江</td><td>绍兴</td><td>1</td><td>0</td><td>0</td><td>0</td></tr>
<tr><td>浙江</td><td>金华</td><td>1</td><td>0</td><td>0</td><td>0</td></tr>
<tr><td>北京</td><td>外地来京人员</td><td>10</td><td>0</td><td>0</td><td>0</td></tr>
<tr><td>北京</td><td>海淀</td><td>6</td><td>0</td><td>0</td><td>0</td></tr>
<tr><td>北京</td><td>朝阳</td><td>5</td><td>0</td><td>0</td><td>0</td></tr>
<tr><td>北京</td><td>西城</td><td>4</td><td>0</td><td>0</td><td>0</td></tr>
<tr><td>北京</td><td>昌平</td><td>3</td><td>0</td><td>0</td><td>0</td></tr>
<tr><td>北京</td><td>大兴</td><td>2</td><td>0</td><td>1</td><td>0</td></tr>
<tr><td>北京</td><td>丰台</td><td>2</td><td>0</td><td>0</td><td>0</td></tr>
<tr><td>北京</td><td>通州</td><td>2</td><td>0</td><td>0</td><td>0</td></tr>
<tr><td>北京</td><td>石景山</td><td>1</td><td>0</td><td>0</td><td>0</td></tr>
<tr><td>北京</td><td>顺义</td><td>1</td><td>0</td><td>0</td><td>0</td></tr>
<tr><td>重庆</td><td>万州区</td><td>3</td><td>0</td><td>0</td><td>0</td></tr>
<tr><td>重庆</td><td>巫山县</td><td>3</td><td>0</td><td>0</td><td>0</td></tr>
<tr><td>重庆</td><td>长寿区</td><td>3</td><td>0</td><td>0</td><td>0</td></tr>
<tr><td>重庆</td><td>垫江县</td><td>2</td><td>0</td><td>0</td><td>0</td></tr>
<tr><td>重庆</td><td>永川区</td><td>2</td><td>0</td><td>0</td><td>0</td></tr>
<tr><td>重庆</td><td>九龙坡区</td><td>2</td><td>0</td><td>0</td><td>0</td></tr>
<tr><td>重庆</td><td>渝北区</td><td>2</td><td>0</td><td>0</td><td>0</td></tr>
<tr><td>重庆</td><td>开州区</td><td>2</td><td>0</td><td>0</td><td>0</td></tr>
<tr><td>重庆</td><td>涪陵区</td><td>1</td><td>0</td><td>0</td><td>0</td></tr>
<tr><td>重庆</td><td>大渡口区</td><td>1</td><td>0</td><td>0</td><td>0</td></tr>
<tr><td>重庆</td><td>忠县</td><td>1</td><td>0</td><td>0</td><td>0</td></tr>
<tr><td>重庆</td><td>云阳县</td><td>1</td><td>0</td><td>0</td><td>0</td></tr>
<tr><td>重庆</td><td>奉节县</td><td>1</td><td>0</td><td>0</td><td>0</td></tr>
<tr><td>重庆</td><td>巫溪县</td><td>1</td><td>0</td><td>0</td><td>0</td></tr>
<tr><td>重庆</td><td>秀山县</td><td>1</td><td>0</td><td>0</td><td>0</td></tr>
<tr><td>重庆</td><td>两江新区</td><td>1</td><td>0</td><td>0</td><td>0</td></tr>
<tr><td>湖南</td><td>长沙</td><td>8</td><td>0</td><td>0</td><td>0</td></tr>
<tr><td>湖南</td><td>永州</td><td>4</td><td>0</td><td>0</td><td>0</td></tr>
<tr><td>湖南</td><td>怀化</td><td>3</td><td>0</td><td>0</td><td>0</td></tr>
<tr><td>湖南</td><td>岳阳</td><td>3</td><td>0</td><td>0</td><td>0</td></tr>
<tr><td>湖南</td><td>娄底</td><td>3</td><td>0</td><td>0</td><td>0</td></tr>
<tr><td>湖南</td><td>郴州</td><td>1</td><td>0</td><td>0</td><td>0</td></tr>
<tr><td>湖南</td><td>株洲</td><td>1</td><td>0</td><td>0</td><td>0</td></tr>
<tr><td>湖南</td><td>湘潭</td><td>1</td><td>0</td><td>0</td><td>0</td></tr>
<tr><td>四川</td><td>成都</td><td>7</td><td>0</td><td>0</td><td>0</td></tr>
<tr><td>四川</td><td>广安</td><td>2</td><td>0</td><td>0</td><td>0</td></tr>
<tr><td>四川</td><td>绵阳</td><td>2</td><td>0</td><td>0</td><td>0</td></tr>
<tr><td>四川</td><td>达州</td><td>1</td><td>0</td><td>0</td><td>0</td></tr>
<tr><td>四川</td><td>德阳</td><td>1</td><td>0</td><td>0</td><td>0</td></tr>
<tr><td>四川</td><td>遂宁</td><td>1</td><td>0</td><td>0</td><td>0</td></tr>
<tr><td>四川</td><td>雅安</td><td>1</td><td>0</td><td>0</td><td>0</td></tr>
<tr><td>山东</td><td>青岛</td><td>4</td><td>0</td><td>0</td><td>0</td></tr>
<tr><td>山东</td><td>威海</td><td>2</td><td>0</td><td>0</td><td>0</td></tr>
<tr><td>山东</td><td>临沂</td><td>2</td><td>0</td><td>0</td><td>0</td></tr>
<tr><td>山东</td><td>济南</td><td>2</td><td>0</td><td>0</td><td>0</td></tr>
<tr><td>山东</td><td>烟台</td><td>2</td><td>0</td><td>0</td><td>0</td></tr>
<tr><td>山东</td><td>潍坊</td><td>1</td><td>0</td><td>0</td><td>0</td></tr>
<tr><td>山东</td><td>日照</td><td>1</td><td>0</td><td>0</td><td>0</td></tr>
<tr><td>山东</td><td>济宁</td><td>1</td><td>0</td><td>0</td><td>0</td></tr>
<tr><td>安徽</td><td>合肥</td><td>6</td><td>0</td><td>0</td><td>0</td></tr>
<tr><td>安徽</td><td>六安</td><td>2</td><td>0</td><td>0</td><td>0</td></tr>
<tr><td>安徽</td><td>阜阳</td><td>2</td><td>0</td><td>0</td><td>0</td></tr>
<tr><td>安徽</td><td>滁州</td><td>1</td><td>0</td><td>0</td><td>0</td></tr>
<tr><td>安徽</td><td>亳州</td><td>1</td><td>0</td><td>0</td><td>0</td></tr>
<tr><td>安徽</td><td>安庆</td><td>1</td><td>0</td><td>0</td><td>0</td></tr>
<tr><td>安徽</td><td>池州</td><td>1</td><td>0</td><td>0</td><td>0</td></tr>
<tr><td>安徽</td><td>蚌埠</td><td>1</td><td>0</td><td>0</td><td>0</td></tr>
<tr><td>广西</td><td>北海</td><td>6</td><td>0</td><td>0</td><td>0</td></tr>
<tr><td>广西</td><td>柳州</td><td>2</td><td>0</td><td>0</td><td>0</td></tr>
<tr><td>广西</td><td>桂林</td><td>2</td><td>0</td><td>0</td><td>0</td></tr>
<tr><td>广西</td><td>梧州</td><td>1</td><td>0</td><td>0</td><td>0</td></tr>
<tr><td>广西</td><td>百色</td><td>1</td><td>0</td><td>0</td><td>0</td></tr>
<tr><td>广西</td><td>河池</td><td>1</td><td>0</td><td>0</td><td>0</td></tr>
<tr><td>福建</td><td>福州</td><td>5</td><td>0</td><td>0</td><td>0</td></tr>
<tr><td>福建</td><td>厦门</td><td>3</td><td>0</td><td>0</td><td>0</td></tr>
<tr><td>福建</td><td>泉州</td><td>1</td><td>0</td><td>0</td><td>0</td></tr>
<tr><td>福建</td><td>宁德</td><td>1</td><td>0</td><td>0</td><td>0</td></tr>
<tr><td>河南</td><td>郑州</td><td>3</td><td>0</td><td>0</td><td>0</td></tr>
<tr><td>河南</td><td>巩义</td><td>2</td><td>0</td><td>0</td><td>0</td></tr>
<tr><td>河南</td><td>洛阳</td><td>1</td><td>0</td><td>0</td><td>0</td></tr>
<tr><td>河南</td><td>三门峡</td><td>1</td><td>0</td><td>0</td><td>0</td></tr>
<tr><td>河南</td><td>信阳</td><td>1</td><td>0</td><td>0</td><td>0</td></tr>
<tr><td>河南</td><td>周口</td><td>1</td><td>0</td><td>0</td><td>0</td></tr>
<tr><td>江苏</td><td>南京</td><td>3</td><td>0</td><td>0</td><td>0</td></tr>
<tr><td>江苏</td><td>苏州</td><td>2</td><td>0</td><td>0</td><td>0</td></tr>
<tr><td>江苏</td><td>连云港</td><td>1</td><td>0</td><td>0</td><td>0</td></tr>
<tr><td>江苏</td><td>扬州</td><td>1</td><td>0</td><td>0</td><td>0</td></tr>
<tr><td>江苏</td><td>南通</td><td>1</td><td>0</td><td>0</td><td>0</td></tr>
<tr><td>江苏</td><td>无锡</td><td>1</td><td>0</td><td>0</td><td>0</td></tr>
<tr><td>海南</td><td>海口</td><td>3</td><td>0</td><td>0</td><td>0</td></tr>
<tr><td>海南</td><td>三亚</td><td>2</td><td>0</td><td>0</td><td>0</td></tr>
<tr><td>海南</td><td>万宁</td><td>2</td><td>0</td><td>0</td><td>0</td></tr>
<tr><td>海南</td><td>临高县</td><td>1</td><td>0</td><td>0</td><td>0</td></tr>
<tr><td>江西</td><td>南昌</td><td>2</td><td>0</td><td>0</td><td>0</td></tr>
<tr><td>江西</td><td>抚州</td><td>1</td><td>0</td><td>0</td><td>0</td></tr>
<tr><td>江西</td><td>萍乡</td><td>1</td><td>0</td><td>0</td><td>0</td></tr>
<tr><td>江西</td><td>九江</td><td>1</td><td>0</td><td>0</td><td>0</td></tr>
<tr><td>江西</td><td>新余</td><td>1</td><td>0</td><td>0</td><td>0</td></tr>
<tr><td>江西</td><td>吉安</td><td>1</td><td>0</td><td>0</td><td>0</td></tr>
<tr><td>陕西</td><td>西安</td><td>2</td><td>0</td><td>0</td><td>0</td></tr>
<tr><td>陕西</td><td>咸阳</td><td>1</td><td>0</td><td>0</td><td>0</td></tr>
<tr><td>陕西</td><td>安康</td><td>1</td><td>0</td><td>0</td><td>0</td></tr>
<tr><td>陕西</td><td>延安</td><td>1</td><td>0</td><td>0</td><td>0</td></tr>
<tr><td>黑龙江</td><td>牡丹江</td><td>1</td><td>0</td><td>0</td><td>0</td></tr>
<tr><td>黑龙江</td><td>哈尔滨</td><td>1</td><td>0</td><td>0</td><td>0</td></tr>
<tr><td>黑龙江</td><td>大庆</td><td>1</td><td>0</td><td>0</td><td>0</td></tr>
<tr><td>黑龙江</td><td>绥化</td><td>1</td><td>0</td><td>0</td><td>1</td></tr>
<tr><td>辽宁</td><td>沈阳</td><td>2</td><td>0</td><td>0</td><td>0</td></tr>
<tr><td>辽宁</td><td>大连</td><td>1</td><td>0</td><td>0</td><td>0</td></tr>
<tr><td>辽宁</td><td>朝阳</td><td>1</td><td>0</td><td>0</td><td>0</td></tr>
<tr><td>贵州</td><td>贵阳</td><td>1</td><td>0</td><td>0</td><td>0</td></tr>
<tr><td>贵州</td><td>铜仁</td><td>1</td><td>0</td><td>0</td><td>0</td></tr>
<tr><td>贵州</td><td>黔南州</td><td>1</td><td>0</td><td>0</td><td>0</td></tr>
<tr><td>吉林</td><td>长春</td><td>1</td><td>0</td><td>0</td><td>0</td></tr>
<tr><td>吉林</td><td>吉林</td><td>1</td><td>0</td><td>0</td><td>0</td></tr>
<tr><td>吉林</td><td>松原</td><td>1</td><td>0</td><td>0</td><td>0</td></tr>
<tr><td>云南</td><td>昆明</td><td>2</td><td>0</td><td>0</td><td>0</td></tr>
<tr><td>宁夏</td><td>银川</td><td>1</td><td>0</td><td>0</td><td>0</td></tr>
<tr><td>宁夏</td><td>中卫</td><td>1</td><td>0</td><td>0</td><td>0</td></tr>
<tr><td>河北</td><td>石家庄</td><td>1</td><td>0</td><td>0</td><td>0</td></tr>
<tr><td>河北</td><td>沧州</td><td>1</td><td>0</td><td>0</td><td>1</td></tr>
<tr><td>甘肃</td><td>兰州</td><td>1</td><td>0</td><td>0</td><td>0</td></tr>
<tr><td>甘肃</td><td>白银</td><td>1</td><td>0</td><td>0</td><td>0</td></tr>
<tr><td>山西</td><td>太原</td><td>1</td><td>0</td><td>0</td><td>0</td></tr>
<tr><td>内蒙古</td><td>满洲里</td><td>1</td><td>0</td><td>0</td><td>0</td></tr></table>

