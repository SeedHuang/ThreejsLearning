# Threejs 学习笔记

# 创建一个场景
本篇的目标是时间段的介绍一下three.js，我们先建立一个场景用以展示一个旋转立方体。万一你卡壳了下面会提供一个可以运行的例子。

## 开始之前
在我们开始使用three.js之前，你需要有个地方去展示它，把下面的Html复制到你的电脑上，然后在复制一份three.js到js/directory下面在打开你的浏览器。
```html
<!DOCTYPE html>
<html>
	<head>
		<meta charset=utf-8>
		<title>My first three.js app</title>
		<style>
			body { margin: 0; }
			canvas { width: 100%; height: 100% }
		</style>
	</head>
	<body>
		<script src="js/three.js"></script>
		<script>
			// Our Javascript will go here.
		</script>
	</body>
</html>
```
万事OK。

## 创建场景
想要使用three.js来显示一个物体需要三样东西：场景（scene），镜头（camera）和渲染期（renderer），在此之上我们可以用镜头来渲染场景。
> 是不是有点晕，Talking is cheap，Show you the code
```
var scene = new THREE.Scene();
var camera = new THREE.PerspectiveCamera( 75, window.innerWidth / window.innerHeight, 0.1, 1000 );

var renderer = new THREE.WebGLRenderer();
renderer.setSize( window.innerWidth, window.innerHeight );
document.body.appendChild( renderer.domElement );
```
