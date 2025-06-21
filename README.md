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

The hero 

## Information

## Quote Section

## Modal

## Footer