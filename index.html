<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">
<html xmlns="http://www.w3.org/1999/xhtml">
<head>
<meta http-equiv="Content-Type" content="text/html; charset=gb2312" />
<meta name="keywords" content="百度地图,百度地图API，百度地图自定义工具，百度地图所见即所得工具" />
<meta name="description" content="百度地图API自定义地图，帮助用户在可视化操作下生成百度地图" />
<title>百度地图API自定义地图</title>
<!--引用百度地图API-->
<style type="text/css">
    html,body{margin:0;padding:0;}
    .iw_poi_title {color:#CC5522;font-size:14px;font-weight:bold;overflow:hidden;padding-right:13px;white-space:nowrap}
    .iw_poi_content {font:12px arial,sans-serif;overflow:visible;padding-top:4px;white-space:-moz-pre-wrap;word-wrap:break-word}
</style>
<script type="text/javascript" src="http://api.map.baidu.com/api?key=&v=1.1&services=true"></script>
</head>

<body>
  <!--百度地图容器-->
  <div style="width:697px;height:550px;border:#ccc solid 1px;" id="dituContent"></div>
</body>
<script type="text/javascript">
    //创建和初始化地图函数：
    function initMap(){
        createMap();//创建地图
        setMapEvent();//设置地图事件
        addMapControl();//向地图添加控件
        addMarker();//向地图中添加marker
        addPolyline();//向地图中添加线
    }
    
    //创建地图函数：
    function createMap(){
        var map = new BMap.Map("dituContent");//在百度地图容器中创建一个地图
        var point = new BMap.Point(117.218827,37.023592);//定义一个中心点坐标
        map.centerAndZoom(point,7);//设定地图的中心点和坐标并将地图显示在地图容器中
        window.map = map;//将map变量存储在全局
    }
    
    //地图事件设置函数：
    function setMapEvent(){
        map.enableDragging();//启用地图拖拽事件，默认启用(可不写)
        map.enableScrollWheelZoom();//启用地图滚轮放大缩小
        map.enableDoubleClickZoom();//启用鼠标双击放大，默认启用(可不写)
        map.enableKeyboard();//启用键盘上下左右键移动地图
    }
    
    //地图控件添加函数：
    function addMapControl(){
        //向地图中添加缩放控件
	var ctrl_nav = new BMap.NavigationControl({anchor:BMAP_ANCHOR_TOP_LEFT,type:BMAP_NAVIGATION_CONTROL_LARGE});
	map.addControl(ctrl_nav);
        //向地图中添加缩略图控件
	var ctrl_ove = new BMap.OverviewMapControl({anchor:BMAP_ANCHOR_BOTTOM_RIGHT,isOpen:1});
	map.addControl(ctrl_ove);
        //向地图中添加比例尺控件
	var ctrl_sca = new BMap.ScaleControl({anchor:BMAP_ANCHOR_BOTTOM_LEFT});
	map.addControl(ctrl_sca);
    }
    
    //标注点数组
    var markerArr = [{title:"牛角岭盘山公路",content:"我的备注",point:"118.313857|36.652226",isOpen:0,icon:{w:21,h:21,l:0,t:0,x:6,lb:5}}
		 ,{title:"威海滨海公路",content:"我的备注",point:"122.147933|37.553303",isOpen:0,icon:{w:21,h:21,l:0,t:0,x:6,lb:5}}
		 ,{title:"青岛胶州湾大桥",content:"我的备注",point:"120.374894|36.16571",isOpen:0,icon:{w:21,h:21,l:0,t:0,x:6,lb:5}}
		 ,{title:"日照玫瑰大道",content:"我的备注",point:"119.568391|35.41407",isOpen:0,icon:{w:21,h:21,l:0,t:0,x:6,lb:5}}
		 ,{title:"开发区环岛路",content:"我的备注",point:"120.263005|35.982496",isOpen:0,icon:{w:21,h:21,l:0,t:0,x:6,lb:5}}
		 ];
    //创建marker
    function addMarker(){
        for(var i=0;i<markerArr.length;i++){
            var json = markerArr[i];
            var p0 = json.point.split("|")[0];
            var p1 = json.point.split("|")[1];
            var point = new BMap.Point(p0,p1);
			var iconImg = createIcon(json.icon);
            var marker = new BMap.Marker(point,{icon:iconImg});
			var iw = createInfoWindow(i);
			var label = new BMap.Label(json.title,{"offset":new BMap.Size(json.icon.lb-json.icon.x+10,-20)});
			marker.setLabel(label);
            map.addOverlay(marker);
            label.setStyle({
                        borderColor:"#808080",
                        color:"#333",
                        cursor:"pointer"
            });
			
			(function(){
				var index = i;
				var _iw = createInfoWindow(i);
				var _marker = marker;
				_marker.addEventListener("click",function(){
				    this.openInfoWindow(_iw);
			    });
			    _iw.addEventListener("open",function(){
				    _marker.getLabel().hide();
			    })
			    _iw.addEventListener("close",function(){
				    _marker.getLabel().show();
			    })
				label.addEventListener("click",function(){
				    _marker.openInfoWindow(_iw);
			    })
				if(!!json.isOpen){
					label.hide();
					_marker.openInfoWindow(_iw);
				}
			})()
        }
    }
    //创建InfoWindow
    function createInfoWindow(i){
        var json = markerArr[i];
        var iw = new BMap.InfoWindow("<b class='iw_poi_title' title='" + json.title + "'>" + json.title + "</b><div class='iw_poi_content'>"+json.content+"</div>");
        return iw;
    }
    //创建一个Icon
    function createIcon(json){
        var icon = new BMap.Icon("http://app.baidu.com/map/images/us_mk_icon.png", new BMap.Size(json.w,json.h),{imageOffset: new BMap.Size(-json.l,-json.t),infoWindowOffset:new BMap.Size(json.lb+5,1),offset:new BMap.Size(json.x,json.h)})
        return icon;
    }
//标注线数组
    var plPoints = [{style:"solid",weight:6,color:"#000",opacity:1,points:["120.120748|36.082525","120.165016|36.125915","120.254703|36.167417","120.346115|36.178605","120.382909|36.159025","120.382335|36.159958"]}
		 ,{style:"solid",weight:5,color:"#000",opacity:1,points:["122.032954|37.526328","122.058251|37.538232","122.059975|37.545557","122.070324|37.540979","122.084122|37.53869","122.103669|37.543726","122.09332|37.545557","122.125516|37.553797","122.137589|37.561578","122.16691|37.533654","122.136439|37.510757","122.137014|37.514879"]}
		 ,{style:"solid",weight:5,color:"#000",opacity:1,points:["117.55833|36.466798","117.570691|36.443343","117.569253|36.423366","117.582764|36.408031","117.60921|36.410587","117.621283|36.419184","117.607485|36.437304","117.599724|36.450775","117.581614|36.460064","117.566091|36.453562","117.564941|36.453562"]}
		 ,{style:"solid",weight:5,color:"#000",opacity:1,points:["118.315151|36.652458","118.305377|36.645625","118.305521|36.644582","118.291005|36.638038"]}
		 ,{style:"solid",weight:5,color:"#000",opacity:1,points:["120.246907|35.971748","120.210688|35.935285","120.188841|35.911435","120.187116|35.899273","120.206663|35.913306","120.210113|35.930142","120.244033|35.958661","120.286002|35.977823","120.313598|35.98016","120.314748|36.014266","120.2952|36.014266","120.274503|35.982964","120.247482|35.970346","120.248632|35.968944"]}
		 ];
    //向地图中添加线函数
    function addPolyline(){
		for(var i=0;i<plPoints.length;i++){
			var json = plPoints[i];
			var points = [];
			for(var j=0;j<json.points.length;j++){
				var p1 = json.points[j].split("|")[0];
				var p2 = json.points[j].split("|")[1];
				points.push(new BMap.Point(p1,p2));
			}
			var line = new BMap.Polyline(points,{strokeStyle:json.style,strokeWeight:json.weight,strokeColor:json.color,strokeOpacity:json.opacity});
			map.addOverlay(line);
		}
	}
    
    initMap();//创建和初始化地图
</script>
</html>


















Having trouble with Pages? Check out our [documentation](https://help.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.
