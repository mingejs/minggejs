# minggeJS

 English version is [here](README_en.md).

# 又迎来1.7.3版更新
有只叫"鲁小夫"的贱渣，他是知乎网的，你绝对是个贱渣+败类
他拿我的事件方法出来喷， 那告诉你写事件方法当时，我只是简单马虎写了几句，前后时间用了一小时左右，结果被喷得一文不值。
好吧，最多的借口都是借口，那么今天特意把事件方法全部重写了

$(XXX).bind("click",function())        绑定$(XXX).bind("click",function()) 绑定
 
$(XXX).bind()                          全部解开绑定

$(XXX).bind("click")                   只解开click绑定

$(XXX).bind(function)                  解开所有该函数（只接受静态函数） 

$(XXX).bind({click:function(){}})      接受OBJECT对象批量传入批量事件
 
$(XXX).one("click",function())        只执行一次后解绑事件

on方法和bind，一样，我只是$.on=$.bind;掩耳法，

off方法和unbid一样，我只是$.off=$.unbind;掩耳法，
 
那么说吧，我没写on委托事件方法，因为我没有重新定义event方法，如果不重新定义过event,事件委托写了也白写，这个只能以后再加了，我时间很有限。

event 我只作了简单处理: event || window.event 。如果用户需要事件委托，那就要麻烦你在事件callback内自己写逻辑了！其实也很简单吧


然后说说，JSONP，同时触发JSONP时，引起公共变量被占用的问题。已修复， 
当公共变量被占用时，线程会等待公用变量消失，如果超时就关闭所有线程
如果用户不设置超时，那么程序默认只等待连接30次！这个方案，应该是无可挑剔了

$.getJSON 或$.ajax 进行测试吧 示例
$.getJSON("http://xxxx?callback=?",function(v){alert(v)});})

另外再到$.toJSON问题，我记得这个问题我修复了三次，一直走漏眼
感谢提交这个问题的网友，我不记得你叫什么名字，连续多次用\t\n\r\b " \这些符号来阴我，你够狠的。有问题就是我自己考虑不周，我不怪你
另外再有位叫"老雷"的网友说"如果不会修复就去百度下载JSON转换程序"，我就笑了，这样的功能，我还需要去百度！

拿这段去测试
alert($.toJSON({"  a%s'\n我好122\n   \d\f\t\b\g\q ":"a%s'\n\n你222好\d\f\t\b\g\q"}))	;
    现在的代码差不多1700行了，压缩文件快接近30K了，可能有些函数方法考虑不周，逻辑错误，函数漏洞，我写程序某些时候比较粗心大意，某些时候马虎了事，敬请各位多加提点，让我尽快修复。
诸如apply我写成aply "on"+evename 我写成 on+"evename" 等等,这些纯粹是我手误，好吧！解释就是掩饰，技术差就是差不找借口了！
感谢各位对MingGeJS项目的关注，那大家只关注MingGeJS就好，不要关注作者了，我没什么值得你关注的！ 我更不想被关注！进来把我当笑话看的，你可以滚了！
以后对带骨的话，一律删除处理。

---------------FROM mingge   版本号1.7.3


继优秀作品shearphoto截图插件，本人又再推出国产山寨JQUERY，为什么我要开发一个山寨JQUERY？老实说我从来没用过JQUERY，正因为我反感JQUERY。
为什么我反感，因为我完全有开发JQUERY的能力，JQUERY的底层我都了如指掌。
我开发插件一直都是用原生JS，大家可以看下我前面的作品shearphoto就是用原生JS写的。  虽说我反感JQUERY，但是JQUERY却在前端界占有大量的用户份额，之后我有个想法，不如重新开发一个属于自己思想，自己架构的JQUERY。有了想法就要实现我山寨JQUERY之路
继优秀作品shearphoto截图插件，本人又再推出国产山寨jQuery，为什么我要开发一个山寨jQuery？老实说我从来没用过jQuery，正因为我反感jQuery。
为什么我反感，因为我完全有开发jQuery的能力，jQuery的底层我都了如指掌。
我开发插件一直都是用原生JS，大家可以看下我前面的作品shearphoto就是用原生JS写的。  虽说我反感jQuery，但是jQuery却在前端界占有大量的用户份额，之后我有个想法，不如重新开发一个属于自己思想，自己架构的jQuery。有了想法就要实现我山寨jQuery之路

我给了他一个霸气的名字：MingGeJs，  

MingGeJs是什么？它是我一个星期完成的作品，它是一个JS类库，它拥有和jQuery相同的语法，相同函数，相同的函数用法， 但是动画，选择器性能，函数
效率都在JQ之上，同时兼容IE 6 7 8，同时与jQuery相兼容

它的名字叫MingGeJs，MingGe就是我的大名， 一看到插件名字，就知道作者是我，知道它是国产的，让别人知道国产类库一样做得很出色，出众

本人文化程度不高，初中毕业！半句英文都不会，但是我相信只要肯努力一样可以实现自己的梦想。MingGeJS的梦想有点大胆，就是在全球范围内，占据

jQuery百分之50以上的用户份额。MingGeJs已在GIT开源，欢迎各路前端高手对MingGeJs类库进行评测！  

我是mingge    请支持国产minggeJS类库，因为我们都是中国人。    

#迎来minggeJS1.7的更新
感谢GIT贡献者提交的BUG，1.6BUG较多，因为当时写得比较急，目前已经大致修复！
minggeJS新增了JSONP，attr()等许多还没及时写上的API,以及优化部份函数等
欢迎大家也到我GIT贡献一下，让我能及时修复更新！

上一次发的1.6版本，并没有介绍到minggeJS的优点，所以很多人只围绕着我山寨jQuery装逼没前途咬着不放，
我说过minggeJS的梦想要夺取JQ百分之50的份额，这话我能写得出，就不会收回，即管失败了我也没损失。 jQuery又不会因为我要挑战他而大怒，失败就失败，又不是没试过！
我还山寨angularjs，开发进度到了百之20左右，我到时候又要开源了。对手多强大我压根不屑，挑战就挑战！

下面我介绍一下minggeJS几大优点。

minggeJS具有以下优点
1：选择器执行速度胜出jQuery，
   以十万个DIV节点测试，分别用minggeJS与jQuery选择器取出指定节点测试：
 jQuery结果 ：     IE7以上：花时1800毫秒   IE7 花时   8135毫秒     IE6   花时超过30-40秒之间，浏览器随机卡死。
 minggeJS结果：    IE7以上：花时1500毫秒   IE7花时    5132毫秒      IE6花时 23-35秒之间   浏览器也有卡死现象，但次数少。
  花时越少，选择器性能越强，从结果来看，minggeJS大获全胜。    司徒正美也开发了一个号称世界最快的选择器，我也测试了下，从结果来看和我不分上下的！
  还有一点值得提提，居闻jQuery的选择器不是自己公司原创的，是用第三方选择器改出来的！minggeJS的选择器问心无愧地说全部是我原创开发的   

2：众所周之，JQUERY的动画原理是采用定时器方原理，minggeJS原理不同，minggeJS的动画采用的是CSS3过渡原理，遗憾的是minggeJS的动画不支持IE678。 minggeJS并不是第一个采用CSS3过渡动画，zepto的动画也是采用这个原理，可惜zepto动画做得真心差，zepto是不支持串联式动画的，用zepto做复杂动画，简直是一大败笔。   minggeJS则支持动画串联，支持高效准确回调，支持接口查询是否正在动画等，可以告诉大家用minggeJS做手机动画，绝对是最佳的选择！      

3：语法，函数用法，函数名称，都与JQUERY一致，只要会JQUERY，你就会更用minggeJS,易学易用，马上上手。部份函数用法稍有不同，例如mingge新建节点是用$(XX).createNode(),比JQUERY方便很多！
  minggeJS不单单是山寨JQUERY，更多的是融入了自己的思想，想法！

4：文件体积20K左右，后期升级可能会维持在40K左右，我自己的想法就是希望不超过40K。

5： minggeJS后期的发展，更多是想往手机端发展，即使战不胜JQUERY，能战胜zepto也是赏心悦目的事。再者就是动画方面，打算采用两种模式供用户选择，1种是CSS3，第2种CSS2定时器方式，定时器方式，估计以插件方式发布！
