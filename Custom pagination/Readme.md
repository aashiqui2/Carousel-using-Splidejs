# This Folder has the custom pagination you can use 
Before doing this, please read the documentation properly <a href="./Readme.md">Documentation Link</a> 

## Steps to be followed:

* Type the script inside the script tag after the js cdn link before the enclosing of tyhe body tag.

```
  <script>
      const splide = new Splide(".splide",{
        perPage:3,
        gap:'1.5rem',
        // This gap is for splide__track
        padding:'3rem', 
        type:'loop',
        drag:'free',
        //draging the image in the corner to see to effect 
        snap:true,
        // pagination:false,
        // autoplay:true
      });

      splide.on("pagination:mounted", function (data) {
        // You can add your class to the UL element
        data.list.classList.add("splide__pagination--custom");

        // `items` contains all dot items
        data.items.forEach(function (item) {
          item.button.textContent = String(item.page + 1);
        });
      });

      splide.mount();
    </script>
```

## Output:

<img src="./Img/pagination.png"/>
