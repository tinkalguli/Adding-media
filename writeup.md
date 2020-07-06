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
