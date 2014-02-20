*This repository is a mirror of the [component](http://component.io) module [danzajdband/zelig](http://github.com/danzajdband/zelig). It has been modified to work with NPM+Browserify. You can install it using the command `npm install npmcomponent/danzajdband-zelig`. Please do not open issues or send pull requests against this repo. If you have issues with this repo, report it to [npmcomponent](https://github.com/airportyh/npmcomponent).*

# zelig

  Classic convolution filters on top of component/convolve

## Available filters

### Zelig#blur()

### Zelig#edgeDetect()

### Zelig#emboss()

### Zelig#laplace()

### Zelig#gaussianBlur()

### Zelig#motionBlur()

### Zelig#sharpen()

## Example

```js
var zelig = require('zelig');
var canvas = document.querySelector('canvas');
var ctx = canvas.getContext('2d');

var img = new Image;
img.onload = draw;
img.src = 'maru.jpg';

function draw() {
  canvas.width = img.width;
  canvas.height = img.height;
  ctx.drawImage(img, 0, 0);
  zelig
    .emboss()
    .canvas(canvas);
}
```

