# scrollLoading
jQuery Scroll load the chart plug-in

1、为每个图表div绑定事件 
 
$(".chart").each(function(index, elem) {
    $(elem).scrollLoading({
        container: $("#report_table"), //滚动对象，监听该对象的滚动事件，很关键。
        callback: function() { //加载到可见范围的回调事件
            loadChart($(elem));
        },
        preloadHeight: 400 //预加载高度
    });
});
2、绑定后，当div在可见范围时，将执行callback方法。

3、可以用于img等标签

4、如果不能滚动加载，需要检查container配置是否正确。

demo：
https://www.jq22.com/yanshi18123
