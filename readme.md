# [ChangeLog]

### Code references
all functions in `index.html`: 

#### Divs with classes (didn't work)
###Red Color Container
```

56	 <h3>Your Selected Colors</h3>
		<ul id="special">
		 <div class="colorContainer" id="red"></div>
		</ul>

```

```

625     window.onload = function() {
        console.log("boilerplate profile");
        // doc elements
        var profileContainer = document.getElementById("profile"),
        postContainer = document.getElementById("posts"),
        colorContainer = document.getElementsByClassName("colorContainer")

```

```

695	 colorContainer.insertAdjacentHTML("beforeend", `
            <li class="colorList"> 
                <a href="./posts/post-${postAndArchive.post.timestamp}.json" id="hexColorLink" class=${showColors} style="color:${postAndArchive.post.colors};">${postAndArchive.post.colors}</a>
            </li>
            `)

```



#### divs with ids (worked)
```

56	 <h3>Your Selected Colors</h3>
		<ul id="special">
		 <div class="colorContainer"></div>
		</ul>

```
```

625     window.onload = function() {
        console.log("boilerplate profile");
        // doc elements
        var profileContainer = document.getElementById("profile"),
        postContainer = document.getElementById("posts"),
        colorContainer = document.getElementsByClassName("colorContainer")

```
```

695	 colorContainer.insertAdjacentHTML("beforeend", `
            <li class="colorList"> 
                <a href="./posts/post-${postAndArchive.post.timestamp}.json" id="hexColorLink" class=${showColors} style="color:${postAndArchive.post.colors};">${postAndArchive.post.colors}</a>
            </li>
            `)

```

#### HTML code
```
<div id="guideTitle">Color Guide</div>

          <a href="javascript:void(0)" class="color-info" id="red-info">Red <span id="arrow">&#9660;</span></a>
            <div class="color-ref" id="red" style="display: none;">
              <span class="description">Red has the ability to rev desire; and not surprisingly when it is the color of fire, danger, and blood on one hand; and love, sexuality and passion on the other.

                  <br><br>
                  In India red is associated with purity, sensuality, and spirituality. On the other hand, some countries in Africa associate red with death, and in Nigeria it represents aggression and vitality. It’s considered a lucky charm in Egypt and symbolizes good fortune and courage in Iran.
              </span>

            <div id="symbolism">
            <h3>Additional Symbolism</h3>
                          <ul>
                            <li>- good fortune (Eastern)</li>
                            <li>- purity (India)</li>
                            <li>- beauty (India)</li>
                            <li>- passion (Western)</li>
                            <li>- strength (Middle East)</li>
                            <li>- life (Japan)</li>
                            <li>- triumph (Cherokee)</li>
                            <li>- sacrifice (Hebrew)</li>
                          </ul>
            </div>


              <h3>Your Selected Colors</h3>
                <ul id="special">
                   <div class="colorContainer" id="red"></div>
                </ul>

</div>
```
### If conditional placement? (Broke code though)

```
538		$('body').on('click','#red-info', function(){
		  $('#red').toggle();

		})

```

or place here?
```
    
694       colorContainer.insertAdjacentHTML("beforeend", `
            <li id="colorList"> 
                <a href="./posts/post-${postAndArchive.post.timestamp}.json" id="hexColorLink" class=${showColors} style="color:${postAndArchive.post.colors};">${postAndArchive.post.colors}</a>
            </li>
            `)

```

