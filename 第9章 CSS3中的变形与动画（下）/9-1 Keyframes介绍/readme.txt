
Keyframes介绍

Keyframes被称为关键帧，其类似于Flash中的关键帧。

在CSS3中其主要以“@keyframes”开头，后面紧跟着是动画名称加上一对花括号“{…}”，括号中就是一些不同时间段样式规则。

@keyframes changecolor{
  0%{
   background: red;
  }
  100%{
    background: green;
  }
}

	在一个“@keyframes”中的样式规则可以由多个百分比构成的，如在“0%”到“100%”之间创建更多个百分比，分别给每个百分比中给需要有动画效果的元素加上不同的样式，从而达到一种在不断变化的效果。

经验与技巧：
	在@keyframes中定义动画名称时，其中0%和100%还可以使用关键词from和to来代表，其中0%对应的是from，100%对应的是to。

浏览器的支持情况：
	Chrome 和 Safari 需要前缀 -webkit-；
	Foxfire 需要前缀 -moz-。
	
案例演示
	通过“@keyframes”声明一个名叫“wobble”的动画，从“0%”开始到“100%”结束，同时还经历了一个“40%”和“60%”两个过程。“wobble”动画在“0%”时元素定位到left为100px，背景色为green，然后在“40%”时元素过渡到left为150px,背景色为orange,接着在“60%”时元素过渡到left为75px，背景色为blue，最后“100%”时结束动画，元素又回到起点left为100px处，背景色变为red。

HTML:
	
	<div>鼠标放到我身上</div>

CSS:

@keyframes wobble {
  0% {
    margin-left: 100px;
    background:green;
  }
  40% {
    margin-left:150px;
    background:orange;
  }
  60% {
    margin-left: 75px;
    background: blue;
  }
  100% {
    margin-left: 100px;
    background: red;
  }
}
div {
  width: 100px;
  height: 100px;
  background:red;
  color: #fff;
}
div:hover{
  animation: wobble 5s ease .1s;
}
 
 
任务:

在CSS编辑器的第1行创建一个动画名叫“changecolor”，在“0%”时背景色为red,在20%时背景色为blue，在40%背景色为orange，在60%背景色为green，在80%时背景色yellow，在100%处时背景色为red。
 
?不会了怎么办
	思考一下，我们刚讲过的Keyframes是否忘记加入前缀了？
	Chrome和Safari:@-webkit-keyframes、-webkit-animation
    Foxfire:@-moz-keyframes、-moz--animation
    
