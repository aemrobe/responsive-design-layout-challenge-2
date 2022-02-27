responisve layout challenge 1

## Table of contents

- [The challenge](#the-challenge)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Continued development](#continued-development)
  - [Useful resources](#useful-resources)
- [Author](#author)

### The challenge

1. your page is divided in to two part the upper part and the lower part you upper part have a div class of (.intro-content) and your lower part have one h2 element and three p elements

2. Keep the text inside (.intro-content)
  in the same place, but have the background
  extend from one side of the viewport
  to the other, no matter how wide or narrow
  the browser is.
3.Limit the maximum width of the text in the
    ower elements which are found in lower part.  

4.  make the .intro-content half of the width of the lower part and put both parts at the center and the text inside both the upper part and lower part should start from the same left position so they will alingn veritically at the center

you have a file path for the screenshot of the design at the bottom

### Screenshot

![](./screenshot.jpg)
file path for the screenshot:
screenshots/responsive layout challenge 2


### Links

- Live Site URL: [Add live site URL here](https://your-live-site-url.com)

## My process

when I make this challenge the thing which was a problem to me is to make the upper part half of the width of  the lower part and still align them horizontally at the center. the text inside both parts should start at the same position as shown above in the screenshot.

when I start doing it
I have
** upper part **
which have a class of the .intro-content
it contain one h1 element and one p element.

```
   HTML
   <div class="intro-content">
             <h1>Lorem ipsum dolor sit.</h1>
             <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Exercitationem aspernatur distinctio laudantium
                 dolores. Nulla quibusdam reprehenderit eum sit minus aliquid!</p>
    </div>
```

** lower part**
which is found at the bottom of the .intro-content It have one h2 element and 3 p elements and I call these elements "lower elements"
``` 
    CSS
        <h2>more content D:</h2>

        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Perferendis, mollitia adipisci magnam voluptatibus
            repellendus fuga ut repellat exercitationem eaque amet, omnis aliquam fugiat laudantium id dicta at? Consectetur
            iure porro illum laudantium excepturi a laborum!
        </p>
        <p>Sit magni soluta porro fugit placeat eius itaque, accusamus quisquam voluptates reiciendis pariatur, vitae
            molestiae.
            Minima, quos reprehenderit autem animi, nisi necessitatibus eligendi quis modi, facilis ipsam nihil odit
            quaerat!
            Nisi doloribus harum culpa ipsam!
        </p>
        <p>Sint corporis animi repudiandae. Aliquid illum, tenetur magnam provident molestiae rem doloremque aspernatur quia
            reiciendis est facilis enim praesentium officia sequi qui debitis exercitationem quaerat hic quos recusandae.
            Architecto repudiandae aperiam tempora iste saepe error.
        </p>
 ```

** the problem I had when i am doing this challenge was to make the .intro-content half of the size of the lower elements placing them at the center while the text inside them start at the same postion at the left **

inorder to solve this problem I should wrap both .intro-content and the lower elements under the .container class. after wrapping them by the .container class we can give max-width to the .container class so the width of both .intro-content and lower elements will be limited because they are wrapped by the container class and we will give a property of margin: 0 auto to the container and both elements the intro-content and the lower elements will be centered.

```
 HTML
<!--upper element -->
<div class="container">
    <div class="intro-content">
        <h1>Lorem ipsum dolor sit.</h1>

          <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Exercitationem aspernatur distinctio laudantium
                 dolores. Nulla quibusdam reprehenderit eum sit minus aliquid!
          </p>
      </div>
</div>
<!--lower element -->
<div class="container">
<h2>more content D:</h2>

     <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Perferendis, mollitia adipisci magnam voluptatibus
         repellendus fuga ut repellat exercitationem eaque amet, omnis aliquam fugiat laudantium id dicta at? Consectetur
         iure porro illum laudantium excepturi a laborum!
     </p>
     <p>Sit magni soluta porro fugit placeat eius itaque, accusamus quisquam voluptates reiciendis pariatur, vitae
         molestiae.
         Minima, quos reprehenderit autem animi, nisi necessitatibus eligendi quis modi, facilis ipsam nihil odit
         quaerat!
         Nisi doloribus harum culpa ipsam!
     </p>
     <p>Sint corporis animi repudiandae. Aliquid illum, tenetur magnam provident molestiae rem doloremque aspernatur quia
         reiciendis est facilis enim praesentium officia sequi qui debitis exercitationem quaerat hic quos recusandae.
         Architecto repudiandae aperiam tempora iste saepe error.
     </p>
</div>
```

```
  CSS
.container{
 max-width: 750px;
 margin: 0 auto;
}

```

after we have done this inorder to make the .intro-content half the width of the the lower element we will give it a width of 50% to the .intro-content.

```
   css
.container {
  max-width: 750px;
  margin: 0 auto;
}

.intro-content {
  width: 50%;
}
```

then inorder to make the background of the .intro-content extend from oneside of the viewport to the other side of the viewport we should wrap the .intro-content with "wrapper" class container and give the background property to .wrapper class because the width of the .intro-content is limited by the container class it doesn't extend from oneside of the viewport to the other side.

```
  HTML
<div class="wrapper">
  <div class="container">
    <div class="intro-content">
      <h1>Lorem ipsum dolor sit.</h1>

      <p>
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Exercitationem
        aspernatur distinctio laudantium dolores. Nulla quibusdam reprehenderit
        eum sit minus aliquid!
      </p>
    </div>
  </div>
</div>

<div class="container">
  <h2>more content D:</h2>

  <p>
    Lorem ipsum dolor sit amet consectetur adipisicing elit. Perferendis,
    mollitia adipisci magnam voluptatibus repellendus fuga ut repellat
    exercitationem eaque amet, omnis aliquam fugiat laudantium id dicta at?
    Consectetur iure porro illum laudantium excepturi a laborum!
  </p>
  <p>
    Sit magni soluta porro fugit placeat eius itaque, accusamus quisquam
    voluptates reiciendis pariatur, vitae molestiae. Minima, quos reprehenderit
    autem animi, nisi necessitatibus eligendi quis modi, facilis ipsam nihil
    odit quaerat! Nisi doloribus harum culpa ipsam!
  </p>
  <p>
    Sint corporis animi repudiandae. Aliquid illum, tenetur magnam provident
    molestiae rem doloremque aspernatur quia reiciendis est facilis enim
    praesentium officia sequi qui debitis exercitationem quaerat hic quos
    recusandae. Architecto repudiandae aperiam tempora iste saepe error.
  </p>
</div>
```

```
  css
.wrapper {
  background: #23424a; /*it give the background as we want */
  color: white;
  padding: 50px 0; /*inorder to add more space above and below the element */
}

.container {
  max-width: 750px;
  margin: 0 auto;
}

.intro-content {
  width: 50%;
}
```

inorder to make it look more good we should give the width for our container class because our container class have only max-width it doesn't have a value for the width . since our container class is a block element it have a width of 100% by default so at smaller screen sizes it won't have a padding at the left at the right so we can give it percentage value for the container class so it will have more space at the left and right at smaller screen sizes. so both the upper element and the lower elemnt will still be responsive and look good.

```
   css
.container {
  width: 80%; /*it will have more space from the right and left at smaller screen sizes */
  max-width: 750px;
  margin: 0 auto;
}
```

### Built with

- Semantic HTML5 markup
- CSS 3

### What I learned

in this challenge I learned we can use the max-width to our element inorder to limit the max-width of our element
this will make our element have a limited width and still be responsive and also I know it is good practice to use a percentage value of width to our element to create more space at the left and the right than using a padding. because if we use padding at the left and right it will look good at the larger screen but when the screen gets smaller that padding will look bigger than the content so instead we should use percentage value of a width and it will look good at every screen sizes.

### Continued development

i want to focus on responsive design,flexbox , grid.

## Author

- frontendmentor - [@aemrobe](https://www.frontendmentor.io/profile/yourusername)
- Twitter - [@Aemro112](https://www.twitter.com/yourusername)
- freecodecamp - [@aemro11]


