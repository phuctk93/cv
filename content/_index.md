---
title: "phuctk93 - Full stack Developer, Desiner for web, app and game."
description: "I am a web & game developer. My knowledge is: HTML, CSS, Javascript (Pure JS, VueJS), TypeScript, Golang, C# (Unity), Python, C++. I can also designer: 3d model, logo, banner,… with free and open source tool like Blender, GIMP, GravitDesigner."
date: 2018-11-18T15:00:18+07:00
---

<div class="columns">
	<div class="column">
		<div class="title" id="title">I'm phuctk93</div>
		<div class="is-size-4 has-text-justified">
		<p>A <b>cross-platform developer</b> for app, web and game with: JavaSript (Vue, TensorflowJS - AI, Pixi, Babylon), CSS (Bulma, Boostrap), HTML (XML, SVG), Golang, C# (Unity - 2D and 3D game engine). </p>
		<p>I'm also <b>designer</b> with open source tools: GIMP, Gravit Designer, Blender. </p>
		<p>
			<a class="button is-dark is-medium" href="#blog">
				<span class="icon">
					<i class="fas fa-book-open"></i>
				</span>
				<span>Blog</span>
			</a>
			<a class="button is-success is-medium" href="#projects">
				<span class="icon">
					<i class="fas fa-tasks"></i>
				</span>
				<span>Project</span>
			</a>
			<a class="button is-danger is-medium" href="#contact">
				<span class="icon">
					<i class="fas fa-address-card"></i>
				</span>
				<span>Contact</span>
			</a>
		</p>
		</div>
	</div>
	<div class="column">
		<svg height="310px" width="210px"><path id="p1" d="m 15.119057,143.16367 c -3e-6,-53.231373 40.614165,-96.383929 90.714283,-96.383931 50.10012,-2e-6 90.71429,43.152555 90.71429,96.383931 0,53.23137 -40.61417,96.38392 -90.71429,96.38392 -50.100114,0 -90.71428,-43.15255 -90.714283,-96.38392 v 150.81252" style="fill:none;fill-opacity:1;stroke:#fff;stroke-width:16;stroke-linecap:round;stroke-linejoin:round;stroke-miterlimit:4;stroke-dasharray:none;stroke-opacity:1" /><path id="p2" d="m 160.2619,145.43155 c 0,22.01118 -10.37403,42.35034 -27.21429,53.35593 -16.84026,11.00559 -37.58831,11.00559 -54.428568,0 C 61.778784,187.78189 51.404757,167.44273 51.404758,145.43155" style="fill:none;stroke:#fff;stroke-width:16;stroke-linecap:round;stroke-linejoin:round;stroke-miterlimit:4;stroke-dasharray:180;stroke-dashoffset:180;stroke-opacity:1"></path></svg>
	</div>
</div>


<script>
	const p1 = document.getElementById('p1'),
	p2 = document.getElementById('p2'),
	title = document.getElementById('title');

	prepareSVG(p1);
	prepareSVG(p2);

	TweenLite.to(p1, 5, {strokeDashoffset: 0});
	TweenLite.to(p2, 2, {strokeDashoffset: 0});
	TweenLite.to(title, 5, {scale: 2, ease: Bounce.easeOut});
	
	function prepareSVG(el) {
		var l = el.getTotalLength();
		el.style.strokeDasharray = l;
		el.style.strokeDashoffset = l;
	}
</script>