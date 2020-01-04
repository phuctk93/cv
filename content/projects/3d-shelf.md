---
title: "Simple 3D Shelf"
date: 2020-01-05T01:31:49+07:00
photo: "/img/projects/3d-shelf.png"
description: "A simple 3d shelf with Blender and Babylonjs"
tags: ["website", "pwa", "babylonjs", "blender", "canvas"]
---
# Simple 3D shelf - A simple 3d shelf with Blender and Babylonjs

This is a simple 3d shelf, I use:

- [Blender](https://www.blender.org/): modeling and export model.

- [Babylonjs](https://www.babylonjs.com/): import and show 3d model to web.

# Live view

<canvas id="renderCanvas" style="width: 100%;height: 100%;touch-action: none;"></canvas>

<script src="https://code.jquery.com/pep/0.4.2/pep.min.js"></script>
<script src="https://cdn.babylonjs.com/babylon.js"></script>
<script src="https://cdn.babylonjs.com/loaders/babylonjs.loaders.min.js"></script>

<script>
  var canvas = document.getElementById("renderCanvas");
  var engine = null;
  var scene = null;
  var createDefaultEngine = function() { return new BABYLON.Engine(canvas, true,{preserveDrawingBuffer: true, stencil: true }); };
  var createScene = function() {
  	var scene = new BABYLON.Scene(engine);
          // Append glTF model to scene.
          BABYLON.SceneLoader.Append("/3d/", "ke_kl.glb", scene, function (scene) {
              
              // Create a default arc rotate camera and light.
              scene.createDefaultCameraOrLight(true, true, true);
              
              // The default camera looks at the back of the asset.
              var helper = scene.createDefaultEnvironment();
              helper.setMainColor(BABYLON.Color3.White());
              // Rotate the camera by 180 degrees to the front of the asset.
              scene.activeCamera.alpha += Math.PI;
          });
          scene.createDefaultCamera()
  	return scene;
  };
  
  
  engine = createDefaultEngine();
  if (!engine) throw 'engine should not be null.';
  scene = createScene();
  engine.runRenderLoop(function () {
      if (scene) {
          scene.render();
      }
  });
  // Resize
  window.addEventListener("resize", function () {
      engine.resize();
  });
</script>
