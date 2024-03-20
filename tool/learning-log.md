# Tool Learning Log

Tool: A-frame

---

3/1/24

During that time, I was struggling how to tinker with A-frame. A-frame was very interesting to me which made me not want to give up on it so I kept trying and but I didn't understand what was the problem. So then I asked my parnther [Kiara](https://github.com/kiaram2249). She told me she used [JsBin](https://jsbin.com/?html,output). When I used Jsbin, it had worked but I was very interesting in how we could do it on the ide. So then I countined to search online but I wasn't sure how to do it. So I'll ask someone else aother day.

---

3/4/24

I went to ask another friend that was doing A-frame too, He said that he would show me but it made me a bit confused on doing it. So then I went back to asking my parther Kiara, since I asked her. She told me that she had made a folder for A-frame in the sandbow but she told me that I shouldn't and make it outside of the sandbox but still in attach with classwork file.I would create a folder called tool and create a folder for A-frame inside the folder and added index.html but oh no, It didn't work. Due to you making it your own folder in the classwork, the IDE didn't allow it because it wasn't a repo. So I asked her again she said to leave it and check to see if the index.html has worked. 

---

3/6/24

I have found the mistake that I have made, it was my spelling. I was looking for my mistake for the past 2 days but I found it. I putted hmtl instead of html, which made me feel very silly but good thing I have found it. So I have removed the *index.hmtl* and added **index.html**. The smallest mistakes can lead to many errors so after fixing my html, It worked! I copied and pasted the a-frame html code and I putted it in the index.html and it has worked! [Example](https://zany-giggle-5gq6q54g54q7c6p-8080.app.github.dev/index.html)

3/12/24

* Today Me and kiara are both working together because we are both working on the same tools, A-frame. This video showed how to change color by using programmatic animation, setting the position, giving the sphere context, and setting texture to your 3D object.
* [Easily code a virtual reality web experience with A-Frame (WebVR)](https://www.youtube.com/watch?v=jhEfT9YjLcU&t=576s)

  The codes I used from the video:
  
```
<script
src="https://cdnjs.cloudflare.com/ajax/libs/aframe/0.5.0/aframe.js">
</script>
<a-scene>
<a-sphere></a-sphere>
<a-plane
src="https://media.giphy.com/media/oYtVHSxngR3lC/giphy.gif"
width="10" height="10" position="0 0 -2.5" color="black"></a-plane>
</a-scene>
<script src="index.js"></script>
$ = (queryString) => document.querySelector(queryString);
const shiftHue = (hue) => (hue + 1) % 360;
let hue = 0;
const animate = () => {
    hue = shiftHue(hue);
    const color = `hsl(${hue}, 100%, 50%)`;
    $(`a-sphere`).setAttribute('color', color);
    const variation = Math.sin(Date.now() / 1000);
    const position = `0 ${1.5 + variation} -2`;
    $('a-sphere').setAttribute('position', position);
    $('a-sphere').setAttribute('rotation', `-90 0`)
    $('a-plane').setAttribute('color', color);

