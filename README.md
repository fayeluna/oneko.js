# oneko.js

Now you can change the cat textures with a dropdown:


### Here is the dropdown you could paste that on your site.
```
<label for="pet-select">Choose a pet:</label>

<select id="pet-select">
  <option value="">--Please choose a variation--</option>
  <option value="original">original</option>
  <option value="trans">trans</option>
  <option value="black-red">black-red</option>
  <option value="orange">orange</option>
  <option value="pink">pink</option>
</select>
```


### Eventlistener to dropdown (also copy into your HTML)
This is the Eventlistener to the dropdown. I also put this in the html directly. Ideally I would also like to put that in the same oneko.js as the other stuff. But I don't know how to do that *yet*.

```
<script>
  function loadOneko(cat) {
    document.getElementById("oneko")?.remove();
    document.getElementById("oneko-script")?.remove();

    const script = document.createElement("script");
    script.id = "oneko-script";
    script.src = "./oneko.js";
    script.dataset.cat = cat || "original";
    document.body.appendChild(script);
  }

  document.getElementById("pet-select").addEventListener("change", function () {
    loadOneko(this.value);
  });

  // Set the starting cat
  loadOneko("trans");
```

Also in your HTML you can put in this script so it can read the dropdown and in the last line
`loadOneko("trans");` you can change out Trans for whatever you would like to be your starting cat to be.

| Cats | Description | Value |
| -------------- | -------------- | -------------- |
| Original Cat | OG cato | original |
| Trans Cat | Trans Texture | trans |
| Anarchy Cat | Black-red Texture | anarchy |
| Orange Cat | Orange cat energy | orange |
| Pink Cat | Pink Texture | pink |

I also plan to add more cats in the future that is something I'm already working on. (I'm currently working on a cat that belongs to a friend :3 )

Here are all the images of the Cats:

## OG Cat
![Original Cat](variants/oneko_original.gif)
## Trans Cat
![Trans Cato](variants/oneko_trans.gif)
## Black - Red Texture Cat
![Anarchy Cat](variants/oneko-anarchy.gif)
## Orange Cat
![Orange Cat](variants/oneko-orange.gif)
## Pink Cat
![Pink Cat](variants/oneko-pink.gif)

---

Original author: https://adryd.com

The Fork I used / cloned: https://github.com/tylxr59/oneko.js/

implemented in a few different places
- https://luna-uwu.neocities.org/ -- my own neocities webpage yayy

All the programming and smart people stuff was done by https://adryd.com and https://github.com/tylxr59 (they also have a very cool page which you can find here: https://tylxr.com/)