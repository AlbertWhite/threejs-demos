### Set up
Create scene, camera, and renderer.

`var scene = new THREE.Scene();
var camera = new THREE.PerspectiveCamera( 20, window.innerWidth / window.innerHeight, 0.01, 1000 );
var renderer = new THREE.WebGLRenderer();
renderer.setSize( window.innerWidth, window.innerHeight );
document.body.appendChild( renderer.domElement );`

In the end, the scene need to be rendered.
`renderer.render(scene, camera);`		

### Add object
To create object, we need *geometry* and *material*. In the end we need to add the object to scene.

For example, while creating a cube:
`var geometry = new THREE.BoxGeometry( 1, 1, 2 );
var material = new THREE.MeshBasicMaterial( { color: 0xffffff } );
var cube = new THREE.Mesh( geometry, material );`

while creating a line:
`var material = new THREE.LineBasicMaterial({ color: 0x0000ff });
var geometry = new THREE.Geometry();
geometry.vertices.push(new THREE.Vector3(-10, 0, 0));
geometry.vertices.push(new THREE.Vector3(0, 10, 0));
geometry.vertices.push(new THREE.Vector3(10, 0, 0));
var line = new THREE.Line(geometry, material);`

