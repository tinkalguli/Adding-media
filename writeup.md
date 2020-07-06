# Adding media

HTML provides ways to add different type of media in the form of images, audio, video. The content from other websites also can be embedded in the form inline frames.

## Adding Images

To embed images we use ```<img>``` tag with "src" and "alt" attribute . The "src" attribute contains the path of the image and "alt" attribute contains description about the image . It is recommned to add alt attribute it helps in seo also incase the image is not displayed the alternative text will be shown to the users.

```
<img src="football.jpg" alt="Two little kids are playing football together" />
```

## Sizing Images

By default image will be dispalyed on a page in it's original size, however we can resize it. There are two ways to resize an image, using width and height attribute on img element and other ways is using CSS.

```
<!-- HTML -->

<img
  src="football.jpg"
  alt="Two little kids are playing football together"
  width="300"
  height="300"
/>
```

```
<!-- CSS -->

img {
  width: 300px;
  height: 300px;
}
```

## Image Formats

We have various image formate, most commonly supported formats are gif, png, jpg, svg. One of the most widely formats are png and jpg. The svg is newly introuduced format which is a vector based image. The quality of svg format does not effect by resizing, unlike other formats. The other formats like png or jpg will lose its quality once you resize it.

>```<img>``` element Vs ```background-image``` property :  The img element is used when the image is part of content and holds some semantic meaning on a page.
The background-image property is used when the image is part of design and directly not relevant to the content of the page.

## Adding Audio

To add audio we use ```<audio>``` element with "src" attribute .

```
<audio src="roar.mp3"></audio>
```

### Audio Attributes

The ```<audio>``` element comes with some other boolean attribute also. Most popular attributes are ```autoplay``` , ```controls```, ```loop``` and ```preload```. By default audio will not show in the website .

If we use autoplay attribute then the audio will play in every reload of the page without showing it or displaying it.

```
<audio autoplay src="roar.mp3"></audio>
```

If we use controls attribute then audio will display with the controls like play, pause, volume etc.

```
<audio controls src="roar.mp3"></audio>
```

The loop attribute will repeat the audio continuously beginning to end and the last preload attribute will identify the information about the audio if there is any. The preload attribute accepts three values: none, auto and metadata. The none value wont preload any information, auto value will preload all the information about the audio(default). The metadata value is in between the none and auto, because it does not preload all the information but few such as clip path's length.

### Audio fallbacks

Different browser support different formats so we have to give fallbacks so that if one format is not supporting then another one will work. To add fallback formats we will remove the src attribute from the audio element. We will use ```<source>``` element with src attribute inside the audio element. There is a type attribute which will define the audio format.

```
<audio controls>
  <source src="roar.ogg" type="audio/ogg" />
  <source src="roar.mp3" type="audio/mpeg" />
  <source src="roar.wav" type="audio/wav" />
  Please <a href="roar.mp3" download>download</a> the audio file.
</audio>
```

## Adding Video Element

Video can be also added on a page using to ```<video>``` element similar to ```<audio>``` element. Works the same way with same attributes(```src```, ```autoplay```, ```controls```, ```loop```, and ```preload```).

However, without controls attribute also the video element will be displayed, but we cannot play or pause. But it can be automatically played with autoplay attribute, without any controls.

```
<video src="earth.ogv" controls></video>
```

### Poster Attribute

This attribute accepts a image url which will show before playing the video.

```
<video src="earth.ogv" controls poster="earth-video-screenshot.jpg"></video>
```

### Video Fallbacks

Unlike the audio video also need fallbacks.

```
<video controls>
  <source src="earth.ogv" type="video/ogg">
  <source src="earth.mp4" type="video/mp4">
  Please <a href="earth.mp4" download>download</a> the video.
</video>
```

## Embeding Video

We can embed a video from "YouTube" or "Vimeo". These websites allow us upload our videos, and allow us to embed our video on a page using inline frame.

```
<iframe
  width="560"
  height="315"
  src="https://www.youtube.com/embed/668nUCeBHyY"
  frameborder="0"
  allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture"
  allowfullscreen
></iframe>
```

### Inline Frames

Inline frame element allow us to embed another HTML page within the current page. To do this ```<iframe>``` tag is used. To add the path of the video, src attribute is used which accepts value in url, which load the page with embeded content. Mainly the iframe element is used to embed media from external websites like YouTube, Google Maps, and others.By default the iframe element comes with default styles like border, width and height. The iframe tag accepts few set of attributes such as frameborder, width, and height, that can be used to style. It can also be styled using CSS properties and value.

```
<iframe
  src="https://www.google.com/maps/embed?pb=!1m14!1m12!1m3!1d3375.919684030991!2d76.3514099151738!3d32.20639478114809!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!5e0!3m2!1sen!2sin!4v1589823959436!5m2!1sen!2sin"
  width="600"
  height="450"
  frameborder="0"
  allowfullscreen=""
  aria-hidden="false"
  tabindex="0"
></iframe>
```

### Figure & Figcaption

The ```<figure>``` and ```<figcaption>``` are newly introduced element to semantically markup self contained content or media.

#### Figure

The ```<figure>``` is block-level element that can wrap self contained element specially media. The element like, images, audio, videos, diagrams, illustrations, etc can be nested inside ```<figure>``` tag.

```
<figure>
  <img src="football.jpg" alt="Two little kids are playing football together" />
</figure>
```

#### Figurecaption

To add a heading or caption inside ```<figure>``` element ```<figcaption>``` tag is used. If we use <figcaption> inside <figure> element then we can avoid alt attribute inimg element.

```
<figure>
  <figcaption>Two little kids are playing football together</figcaption>
  <img src="football.jpg" />
</figure>
```
