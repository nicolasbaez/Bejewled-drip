# Bejewled-drip
They're watching uxxxxx

![buh](https://github.com/nicolasbaez/Bejewled-drip/blob/main/xp018.gif)
```javascript
setup = (_) => createCanvas((w = 500), w, WEBGL);
draw = (_) => {
  colorMode(HSB, 3);
  rotateX(w);
  rotateY(w / 2);
  r = 166;
  noFill();
  beginShape();
  for (i = 0; i < 4; i += 0.01)
    for (j = 0; j < 7; j += 0.1) {
      stroke(noise(i, j, w) * 3, noise(i, j, w) * 9, 3);
      vertex(r * sin(i) * cos(j), r * sin(i) * sin(j), r * cos(i));
    }
  endShape();
  w -= 0.01;
};
keyPressed = (_) => {
  if (key === "s") {
    saveGif("xp018.gif", 700, { delay: 0, units: "frames" });
  }
};
