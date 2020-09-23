<div align="center">

## Drop Down Menu's on Click


</div>

### Description

Advanced Code. With quite a bit of changing this code can be VERY GOOD!!! Try it, if you have a lot of knowledge in internet languages.

Please go to the bottom of this page and vote for me. I would greatly appreciate it. THANK YOU!
 
### More Info
 
Please go to the bottom of this page and vote for me. I would greatly appreciate it. THANK YOU!


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[Mike McNaughton](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/mike-mcnaughton.md)
**Level**          |Advanced
**User Rating**    |4.2 (67 globes from 16 users)
**Compatibility**  |Java \(JDK 1\.2\)
**Category**       |[Links](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/links__2-79.md)
**World**          |[Java](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/java.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/mike-mcnaughton-drop-down-menu-s-on-click__2-2071/archive/master.zip)





### Source Code

```
<script language="JavaScript">
/********************************************************************************
Copyright © 2000 Michro. All rights reserved.
This script may be used freely as long as this message is intact! ********************************************************************************/
var stayFolded=false
var exImg=new Image(); exImg.src='images/arrow10.gif'
var unImg=new Image(); unImg.src='images/arrow1.gif'
var n = (document.layers) ? 1:0;
var ie = (document.all) ? 1:0;
var browser=((n || ie) && parseInt(navigator.appVersion)>=4)
function makeMenu(obj,nest){
	nest=(!nest) ? '':'document.'+nest+'.'
	this.css=(n) ? eval(nest+'document.'+obj):eval('document.all.'+obj+'.style')
 	this.ref=(n) ? eval(nest+'document.'+obj+'.document'):eval('document');
	this.height=n?this.ref.height:eval(obj+'.offsetHeight')
	this.x=(n)? this.css.left:this.css.pixelLeft;this.y=(n)? this.css.top:this.css.pixelTop;
	this.hideIt=b_hideIt;	this.showIt=b_showIt; this.vis=b_vis; this.moveIt=b_moveIt
	return this
}
function b_showIt(){this.css.visibility="visible"}
function b_hideIt(){this.css.visibility="hidden"}
function b_vis(){if(this.css.visibility=="hidden" || this.css.visibility=="hide") return true;}
function b_moveIt(x,y){this.x=x; this.y=y; this.css.left=this.x; this.css.top=this.y}
function init(){
	oTop=new Array()
	oTop[0]=new makeMenu('divTop1','divCont')
	oTop[1]=new makeMenu('divTop2','divCont')
	oTop[2]=new makeMenu('divTop3','divCont')
	oTop[3]=new makeMenu('divTop4','divCont')
	oTop[4]=new makeMenu('divTop5','divCont')
	oTop[5]=new makeMenu('divTop6','divCont')
	oSub=new Array()
	oSub[0]=new makeMenu('divSub1','divCont.document.divTop1')
	oSub[1]=new makeMenu('divSub2','divCont.document.divTop2')
	oSub[2]=new makeMenu('divSub3','divCont.document.divTop3')
	oSub[3]=new makeMenu('divSub4','divCont.document.divTop4')
	oSub[4]=new makeMenu('divSub5','divCont.document.divTop5')
	oSub[5]=new makeMenu('divSub6','divCont.document.divTop6')
	for(i=0;i<oSub.length;i++){ oSub[i].hideIt() }
	for(i=1;i<oTop.length;i++){ oTop[i].moveIt(0,oTop[i-1].y+oTop[i-1].height) }
}
function menu(num){
	if(browser){
		if(!stayFolded){
			for(i=0;i<oSub.length;i++){
				if(i!=num){
					oSub[i].hideIt()
					oTop[i].ref["imgA"+i].src=unImg.src
				}
			}
			for(i=1;i<oTop.length;i++){
				oTop[i].moveIt(0,oTop[i-1].y+oTop[i-1].height)
			}
		}
		if(oSub[num].vis()){
			oSub[num].showIt()
			oTop[num].ref["imgA"+num].src=exImg.src
		}else{
			oSub[num].hideIt()
			oTop[num].ref["imgA"+num].src=unImg.src
		}
		for(i=1;i<oTop.length;i++){
			if(!oSub[i-1].vis()) oTop[i].moveIt(0,oTop[i-1].y+oTop[i-1].height+oSub[i-1].height)
			else oTop[i].moveIt(0,oTop[i-1].y+oTop[i-1].height)
		}
	}
}
if(browser) onload=init;
</script>
<div id="divCont" style="width: 122; height: 211">
	<div id="divTop1" class="clTop"><a href="" onclick="menu(0); return false" class="clMain"><img src="images/arrow1.gif" name="imgA0" width=0 height=0 alt="" border="0"><IMG SRC="http://swo1.hypermart.net/_private/front.gif" width="122" height="21"></a><Br>
		<div id="divSub1" class="clSub" style="width: 63; height: 94">
<!--To change the links, replace the # with the filename or wherever you want the link to go to!-->
			 <a target="Main" href="http://swo1.hypermart.net/join.html" class="clSubb">-Join</a><Br>
			 <a target="Main" href="rules.htm" class="clSubb">-Rules</a><Br>
			 <a target="Main" href="rptips.html" class="clSubb">-Rp Tips</a><Br>
			 <a target="Main" href="begin.html" class="clSubb">-sWo Beginnings</a><Br>
			 <a target="Main" href="hardcore.html" class="clSubb">-sWo Hardcore</a><Br>
<a target="Main" href="htmlhelp.htm" class="clSubb">-sWo HTML Help</a><Br>
		</div>
	</div>
	<div id="divTop2" class="clTop"><a href="" onclick="menu(1); return false" class="clMain"><img src="images/arrow1.gif" name="imgA1" width=0 height=0 alt="" border="0"><IMG SRC="http://swo1.hypermart.net/_private/rp.gif" width="122" height="21"></a><Br>
		<div id="divSub2" class="clSub" style="width: 115; height: 94">
			 <a href="http://iwa-efed.hypermart.net/rpboard" target="_blank" class="clSubb">-Wed/Sat Rp Board</a><Br>
			 <a href="http://swo1.hypermart.net/cgi-bin/index.html" target="_blank" class="clSubb">-PPV Rp Board</a><Br>
			 <a href="http://members2.boardhost.com/pxroy33/" target="_blank" class="clSubb">-OOC Board</a><Br>
			 <a href="http://users3.cgiforme.com/sworpboard/cfmboard.html" target="_blank" class="clSubb">-Back Up Board</a><Br>
			 <a target="Main" href="http://swo1.hypermart.net/cgi-bin/news/index.html" class="clSubb">-News & Rumors Board</a><Br>
		</div>
	</div>
	<div id="divTop3" class="clTop"><a href="" onclick="menu(2); return false" class="clMain"><img src="images/arrow1.gif" name="imgA2" width=0 height=0 alt="" border="0"><IMG SRC="http://swo1.hypermart.net/_private/members.gif" width="122" height="21"></a><Br>
		<div id="divSub3" class="clSub" style="width: 122; height: 94">
			 <a target="Main" href="sworoster.htm" class="clSubb">-Roster</a><Br>
			 <a target="Main" href="titles-rankings.html" class="clSubb">-Titles and Rankings</a><Br>
			 <a target="Main" href="titlehistories.html" class="clSubb">-Title Histories</a><Br>
			 <a target="Main" href="http://swo1.hypermart.net/matchrequest.html" class="clSubb">-Sign a Match</a><Br>
			 <a target="Main" href="http://swo1.hypermart.net/sneak.html" class="clSubb">-Interfear Request</a><Br>
		</div>
	</div>
	<div id="divTop4" class="clTop"><a href="" onclick="menu(3); return false" class="clMain"><img src="images/arrow1.gif" name="imgA3" width=0 height=0 alt="" border="0"><IMG SRC="http://swo1.hypermart.net/_private/results.gif" width="122" height="21"></a><Br>
		<div id="divSub4" class="clSub" style="width: 122; height: 94">
			 <a target="Main" href="http://jjdermont.hypermart.net/wed.html" class="clSubb">-Wed. Revolution</a><Br>
			 <a target="Main" href="sat.html" class="clSubb">-Sat. Combat Zone</a><Br>
			 <a target="Main" href="ppv.htm" class="clSubb">-PPV</a><Br>
			 <a target="Main" href="pastppv.html" class="clSubb">-PPV Archives</a><Br>
		</div>
	</div>
	<div id="divTop5" class="clTop"><a href="" onclick="menu(4); return false" class="clMain"><img src="images/arrow1.gif" name="imgA4" width=0 height=0 alt="" border="0"><IMG SRC="http://swo1.hypermart.net/_private/coming.gif" width="122" height="21"></a><Br>
		<div id="divSub5" class="clSub" style="width: 122; height: 94">
		</div>
	</div>
	<div id="divTop6" class="clTop" style="width: 139; height: 39"><a href="" onclick="menu(5); return false" class="clMain"><img src="images/arrow1.gif" name="imgA5" width=0 height=0 alt="" border="0"><IMG SRC="http://swo1.hypermart.net/_private/coming.gif" width="122" height="21"></a><Br>
		<div id="divSub6" class="clSub" style="width: 79; height: 94">
		</div>
	</div>
 <p>
<!--- Place all page content here --->
</div>
</td>
 </tr>
 <tr><!-- row 3 -->
 </tr>
 <tr><!-- row 4 -->
 </tr>
 <tr><!-- row 5 -->
 </tr>
 <tr><!-- row 6 -->
 </tr>
 <tr><!-- row 7 -->
 </tr>
 <tr><!-- row 8 -->
 </tr>
 <tr><!-- row 9 -->
 </tr>
 <tr><!-- row 10 -->
 </tr>
 <tr><!-- row 11 -->
 </tr>
 <tr><!-- row 12 -->
 </tr>
 <tr><!-- row 13 -->
 </tr>
 <tr><!-- row 14 -->
 </tr>
 <tr><!-- row 15 -->
 </tr>
 <tr><!-- row 16 -->
 </tr>
 <tr><!-- row 17 -->
 </tr>
</table>
```

