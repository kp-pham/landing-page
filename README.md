# landing-page

The landing page project builds upon the markup of documents for creating and structuring the content of webpages with style sheets for the presentation and styling of documents to format the content of webpages. Given an image of the design for a webpage and a reference of the fonts and colors used for the design of the website, recreate the webpage from a blank HTML document and use  a CSS stylesheet to match the design of the original webpage.

## Header

The header is the topmost section of the website. The purpose of the header is to display the header logo and provide links to the other pages of the website.  The structure of the header is a container whose children are containers which represent the 
components of the header such as the header logo and the links in the header.

```
<div class="header">
    <div class="header-logo">Header Logo</div>
    <div class="header-links">
        <ul>
            <li><a href="#">header link one</a></li>
            <li><a href="#">header link two</a></li>
            <li><a href="#">header link three</a></li>
        </ul>
    </div>
</div>
```

The nested containers in the header allow for the use of flexbox to position the header logo towards the left side of the header and the links in the header towards the right side of the header. The container for the header can turned into a flex container and the containers for the header logo and links in the header become flex items which were arranged to be centered vertically and have space between each other and the edge of the screen.


```
.header {
    display: flex;
    align-items: center;
    justify-content: space-around;
}
```

Nested flex containers are flex items which are also flex containers. The use of the unordered list for the links in the header indicate a group of related items for screen readers but create a design problem when displaying the links in the header. The bullet points and list format can be removed when the ```list-style-type``` attribute of the unordered list element is set to ```none``` and the unordered list element is turned into a flex container to arrange the list items with an equal amount of space between them.

```
ul {
    display: flex;
    gap: 20px;
    list-style-type: none;
}
```

## Hero

The hero is the section at the top of the website beneath the header. The purpose of the hero is to capture the attention of the user with an image and statement as the first section the user sees. The structure of the hero is a container to set aside space for the respective section of the page and a container for the hero statement and the placeholder for the image. The hero statement contains the main and secondary text and a button for the user to sign up for the advertised product. The placeholder for the image is represented as an empty container with placeholder text and background.
 

```
<div class="hero-section">
    <div class="hero">
        <div class="hero-content">
            <div class="hero-main-text">This website is awesome</div>
            <div class="hero-secondary-text">
                This website has some subtext that goes here under the main title.
                It's a smaller font and the color in lower contrast.
            </div>
            <button class="hero-sign-up">Sign up</button>
        </div>
        <div class="hero-image">this is a placeholder for an image</div>
     </div>
</div>
```

The use of two separate containers for the hero section and hero allows for the use of flexbox to center the hero and arrange the hero statement and image placeholder with an equal amount of space between them because the hero section is the outermost flex container and the hero is a nested flex container. The outermost flex container centers the nested flex container and the nested flex container arranges the  elements to have an equal amount of space when centered.

```
.hero-section {
    display: flex;
    justify-content: center;
    align-items: center;
}

.hero {
    display: flex;
    width: 1025px;
    gap 40px;
}
```

The use of separate containers for the hero statement and image placeholder allow for the use of flexbox to adjust the width of the flex items within the flex container. The shorthand ```flex``` sets the ```flex-grow```, ```flex-shrink```, and ```flex-basis``` attributes which determines the growth and shrink factor and the percentage of space in the flex container the flex item consumes. The ```flex-grow``` attribute is set to ```1``` for the hero statement and image placeholder because the default value for the ```flex-grow``` attribute is ```0``` and the default value for the ```flex-shrink``` attribute is  ```1```. In other words, flex items can only shrink by default. The ```flex-basis``` attribute for the hero statement is set to a lower percentage than the image placeholder for the image placeholder to take up more space than the hero statement.

```
.hero-content {
    flex: 1 1 90%;
}

.hero-image {
    display: flex;
    flex: 1 1 100%;
    justtify-content: center;
    align-items: center;
}
```

## Information

The information section provides information about the product instead of promoting the product. The purpose of the section is to inform the user behind the purpose of the product and the impact of the product on customers through testimonials and case studies from real customers. The structure of the information section is a container to set aside space for the respective section of the page and containers for the header of the section and the illustrations and accompanying subtext.

```
<div class="information-section">
     <div class="information-header">Some random information.</div>
    <div class="information">
        <div class="card">
            <div class="illustration"></div>
            <div class="subtext">this is some subtext under an illustration or image</div>
        </div>
        <div class="card">
            <div class="illustration"></div>
            <div class="subtext">this is some subtext under an illustration or image</div>
        </div>
        <div class="card">
            <div class="illustration"></div>
            <div class="subtext">this is some subtext under an illustration or image</div>
        </div>
        <div class="card">
            <div class="illustration"></div>
            <div class="subtext">this is some subtext under an illustration or image</div>
        </div>
    </div>
</div>
```

The use of separate containers for the header of the section and the illustrations and accompanying subtext allows for the use of flex to arrange the  flex items in the flex container for the illustrations and accompanying subtext without affecting the formatting for the header of the section. Each illustration and caption is encapsulated within a container which is a flex item of the flex container and are arranged to have an equal amount of space between one another. On the other hand, the text for the header of the section can be centered through text alignment instead of flexbox.

```
.information-center {
    text-align: center;
}

.information {
    display: flex;
    justify-content: center;
    gap: 60px;
}

.card {
    display: flex;
    flex-direction: column;
    gap: 5px;
    width: 175px;
}
```

## Quote Section

## Modal

## Footer