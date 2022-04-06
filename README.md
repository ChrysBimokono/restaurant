
This is an E-commerce Restaurant built using React Framework

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Continued development](#continued-development)
  - [Useful resources](#useful-resources)
- [Author](#author)
- [Acknowledgments](#acknowledgments)



## Overview

### The challenge

After completing the site, 
users should be able to:

- View the optimal layout for each of the website's pages depending on their device's screen size
- Move up and down sections of the website
- Move up and down sections of the website

- See hover states for all interactive elements on the page


### Screenshot
I added a screenshot of my portfolio here.

![](./src/assets/myportfolio.jpeg)



### Links

- Live Site URL: [Add live site URL here](https://pnitschool.netlify.app/)

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- CSS Grid
- Mobile-first workflow
- REACT


### What I learned

I Used this section to recap over some of my major learnings while working through this project. Writing these out and providing code samples of areas i wanted to highlight.

Doing this project:

* I learned to design a web responsive site using React Framework 
* I learned to design a website accessible to different types of users using React Framework
* I used intensively CSS FlexBox LAYOUT.
* I learned how to design a gallery section with React
* I learned how to implement a video section 






```css
/* for someone who is visually impaired */
Made sure to implement this content for only screen readers to help users without vision.

.app__gallery-content{
    flex: 1;
    display: flex;
    justify-content: center;
    align-items: flex-start;
    flex-direction: column;

    min-width: 500px;
    padding-right: 2rem;
}

.app__gallery-content button{
    margin-top: 1rem;
}

.app__gallery-images{
    flex: 1;
    display: flex;
    flex-direction: row;
    max-width: 50%;
    position: relative;
}

.app__gallery-images_container{
    display: flex;
    flex-direction: row;
    width: max-content;
    overflow-x: scroll;
    -ms-overflow-style: none;
    scrollbar-width: none;
}

.app__gallery-images_container::-webkit-scrollbar{
    display: none;
}

.app__gallery-images_card{
    position: relative;
    min-width: 301px;
    height: 447px;
    margin-right: 2rem;
}

.gallery__image-icon{
    position: absolute;
    color: #fff;
    font-size: 2rem;
    opacity: 0.5;
    tra
```
```js
const galleryImages= [images.gallery01,images.gallery02,images.gallery03,images.gallery04]
const Gallery = () => {
   const scrollRef= React.useRef(null);

   const scroll=(direction)=>{
     const {current}= scrollRef;

     if(direction === 'left'){
       current.scrollLeft -= 300;
     } else {
       current.scrollLeft +=300
     }
   }
  return (

    <div className='app__gallery flex__center'>
        <div className='app__gallery-centent'>
          <SubHeading title= "instagram"/>
          <h1 className='headtext__cormorant'>Photo Gallery</h1>
          <p className='p__opensans' style={{color:"#AAA", marginTop:'2rem'}}>Metus vulputate eu scelerisque felis. At erat pellentesque adipiscing commodo elit</p>
          <button type='button' className='custom__button'>View More</button>
        </div>

        <div className='app__gallery-images'>
          <div className='app__gallery-images_container' ref={scrollRef}>
              {galleryImages.map((image,index)=>(
                <div className='app__gallery-images_card flex__center' key={`gallery_image-${index+1}`}>
                  <img src={image} alt='gallery'/>
                  <BsInstagram className='gallery__image-icon'/>
                </div>
              ) )}
          </div>
          <div className='app__gallery-images_arrows'>
            <BsArrowLeftShort className='gallery__arrow-icon'onClick={()=>scroll('left')}/>
            <BsArrowRightShort className='gallery__arrow-icon'onClick={()=>scroll('right')}/>
          </div>
        </div>
     </div>

  );
 
}

export default Nav
```

### Continued development
However, I need to build website using even better and more resuable Reactcodes.


### Useful resources

- [Example resource 1](https://www.youtube.com/kepowob) - This helped me learn how to better use CSS Flex and Grid. I really liked this pattern and will use it going forward.

## Author

- Website - [Chrys-Bimokono](https://chrysbim.com/index.html)

- Twitter - [@EnockBim](https://twitter.com/home)


## Acknowledgments
I really give thanks to the frontend community for their support and encouragement.


