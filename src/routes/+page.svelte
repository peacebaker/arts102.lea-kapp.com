<script>
	import ColorSquare from "../lib/ColorSquare.svelte";
  import "@fontsource/fira-sans";
  import "normalize.css";
	import { slide } from "svelte/transition";

  // 
  let navOpen = true;
  let screenSize;

  // 
  function toggleNav() {
    if (navOpen) {
      navOpen = false;
    } else {
      navOpen = true;
    }
  }
 
  /**
   * Create an array of integers beginning at the "start number" and counting down until the end number.
   * @param start
   * @param end
   * @returns array of integers
   */
  function countdown(start, end) {
    let nums = [];
    for (let i = start; i > end; i--) {
      nums.push(i)
    }
    return nums;
  }
</script>

<div class="container">
  <nav>
    <button on:click={toggleNav}>{#if navOpen}&uarr;{:else}&darr;{/if}</button>
    {#if navOpen}
      <div transition:slide>
        <ul>
          <a href="#first-day">
            <li>First Day</li>
          </a>
          <a href="#elements-of-design">
            <li>Elements of Design</li>
          </a>
          <ul>
            <a href="#line">
              <li>Line</li>
            </a>
            <a href="#texture">
              <li>Texture</li>
            </a>
            <a href="#shape">
              <li>Shape</li>
            </a>
            <a href="#form">
              <li>Form</li>
            </a>
            <a href="#space">
              <li>Space</li>
            </a>
            <a href="#value">
              <li>Value</li>
            </a>
            <a href="#color">
              <li>Color</li>
            </a>
          </ul>
          <a href="#principles-of-design">
            <li>
              Principles of Design
            </li>
          </a>
          <ul>
            <a href="#balance">
              <li>Balance</li>
            </a>
            <a href="#repetition-rhythm-pattern">
              <li>Repetition, Rhythm, and Pattern</li>
            </a>
            <a href="#emphasis-contrast">
              <li>Emphasis and Contrast</li>
            </a>
            <a href="#proportion-scale">
              <li>Proportion and Scale</li>
            </a>
            <a href="#movement">
              <li>Movement</li>
            </a>
            <a href="#unity">
              <li>Unity</li>
            </a>
          </ul>
          <a href="#rgb-color-theory">
            <li>Bonus:  RGB Color Theory</li>
          </a>
          <ul>
            <a href="#color-wheel">
              <li>Color Wheel</li>
            </a>
            <a href="#color-mixing">
              <li>Color Mixing</li>
            </a>
          </ul>
        </ul>
      </div>
    {/if}
  </nav>


  <main>
    <div class="text">
      <h1 id="first-day">First Day</h1>
      <p>When I signed up for ARTS 102 last semester, I figured "this is an intro class – it can't be too hard," so I took the condensed course over the summer semester, despite it being my first ever art class.</p>
      <p>On my first day, I started to panic.  I had heard all of these words before, but in this context, they didn't make sense.  How could art "move" if it's a still image?  Aren't form, space, and shape basically the same thing?</p>
      <p>Worst of all, our instructor said that we needed a sketchbook, and I could not draw – or at least I thought I couldn't draw.  I had tried drawing on several occasions, and every time, the drawings turned out like garbage.  I can't turn in garbage for school!</p>
    </div>
    <div class="iframe-wrapper">
      <iframe src="https://giphy.com/embed/BbBYfhduY1u3m" title="Stressed Spongebob" frameBorder="0" class="giphy-embed" allowFullScreen></iframe>
    </div>
    <div class="credit">
      <a href="https://giphy.com/gifs/spongebob-squarepants-stressed-BbBYfhduY1u3m">via GIPHY</a>
    </div>

    <div class="text">
      <p>But the professor said I could use digital tools, which I felt more comfortable with, and my friend had been talking about Krita for the past several months.  I'm already a Linux junkie, and the fact that one of our tools is leaking into the mainstream made me very excited to try it.  In fact, I already needed a new laptop, so I bought one with a touchscreen specifically for this class.</p>
      <p>Unfortunately, my first attempts were less than stellar.  This is the first drawing I tried to copy from the textbook:</p>
    </div>
    <img src="should_be_easy.webp" alt="an attempt to recreate Picasso's War and Peace">
    <div class="credit">
      [Lea Kapp, 2023]
    </div>
    
    <div class="text">
      <p>I thought it looked easy, but it wasn't.</p>
      <p>I didn't like the results, and I immediately deflated.  Not only was I going to fail this class, but I had also spent an extra I-don't-want-to-think-about-it dollars on this laptop for the touchscreen, and now I'm never going to use it.  Even with practice, I could never get "good" because I didn't know what to practice.  Why did I even try?</p>
      <p>It was a bad night.</p>
      <p>I guess there is some truth to at least that final statement.  If you don't know what to practice, it's incredibly hard to get better.  Fortunately, millions of artists have come before us, leaving methodology and advice that you can follow to grow as an artist.  Within only a few short weeks, you can learn the Elements of Design and Principles of Design, which you can use to make anything look better.</p>
      <p><span class="bold">Author's Note:</span> A keen eye would spot that I purchased a touchscreen laptop to draw digitally, yet all of my drawings are done by hand.  Why is this?  Because when I draw a diagonal, it looks like this:</p>
    </div>
    <img src="squiggly_line.webp" alt="a squiggly line with two arbitrary break points where the pen cut out">
    <div class="credit">
      [Lea Kapp, 2023]
    </div>
    
    <div class="text">
      <p>
        Oh, squiggly line,<br>
        Yes, you, squiggly line:<br>
        Line that doth wiggle<br>
        And jiggle across the page,<br>
        Why doth thou taunt me?
      </p>
  
      <p>
        For my hand is quite steady.<br>
        And my ruler quite straight.<br>
        Yet you, squiggly line,<br>
        Are not.
      </p>
    </div>

    <div class="text">
      <h1 id="elements-of-design">Elements of Design</h1>
      <p>The elements of design are the tools we can use as artists/designers in order to achieve the effects we want.  Many of them are based on English words, but their definitions shift in the context of design.  By utilizing these elements in certain ways, we can create effects that will be universally interpretable, or at least pretty close.</p>
      <p>The elements of design are:</p>
      <ul>
        <li>Line</li>
        <li>Texture</li>
        <li>Shape</li>
        <li>Form</li>
        <li>Space</li>
        <li>Value</li>
        <li>Color</li>
      </ul>

      <h2 id="line">Line</h2>
      <p>My favorite definition for a line that I came across was, "a moving point made by a pointed tool, such as a brush, pen, or stick."  I think the definition is a bit limiting, but it certainly paints a clear picture.  I originally learned about lines in math class, and they had some pretty strict rules about what makes a line a line:</p>
      <ul>
        <li>Must be straight.</li>
        <li>Goes on forever in both directions.</li>
        <li>Probably has a slope or something.</li>
      </ul>
      <p>But those rules don't exist in art class.  In art class, a line is simply a boundary between two things, usually shapes.  Lines can be actual, like the outline of a cartoon character, or implied, like when you shift between colors with no gradient.</p>
    </div>
    <img src="powerpuff_girls.webp" alt="the powerpuff girls logo">
    <div class="credit">
      [Cartoon Network, 1998]
    </div>

    <div class="text">
      <h2 id="texture">Texture</h2>
      <p>Texture describes how a surface feels, or how it would feel if you were allowed to touch it without getting kicked out of the art gallery.  Do not touch the art without explicit permission.  They do not like that.  Like lines, textures don't need to be real – they can also be implied.  When texture describes something intangible, it describes how we imagine it would feel if it were to become a tangible object.</p>
    </div>
    <img src="marbles.jpg" alt="six transparent, blue marbles">
    <div class="credit">
      [pxfuel.com, Undated]
    </div>

    <div class="text">
      <h2 id="shape">Shape</h2>
      <p>A shape is a 2D area that is bound by line, value or color.  It can also be thought of as any flat, enclosed area.  Because the area is 2-Dimensional, all shapes will have a length and a width.  Artists and designers use a combination of geometric and organic shapes to create designs.</p>
    </div>
    <img src="2d_shapes.webp" alt="a cyan circle, a spring green triangle, and a violet rectangle, arranged vaguely in the shape of a face">
    <div class="credit">
      [Lea Kapp, 2023]
    </div>
    

    <div class="text">
      <h2 id="form">Form</h2>
      <p>Form is a 3D area that's bound by line, value, or color.  It's almost the same thing as shape, but 3D instead of 2D.  Since forms are 3D, they have length, they have length, width, and depth.</p>
    </div>
    <div class="iframe-wrapper">
      <iframe src="https://www.youtube-nocookie.com/embed/WhWc3b3KhnY" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
    </div>
    <div class="credit">
      [Blender Studio, 2019]
    </div>

    <div class="text">
      <h2 id="space">Space</h2>
      <p>Space is the distance between objects.  It can be used to create the illusion of depth within a piece of art, or sometimes, the space might be part of the art.  Space can be 2D, 3D, negative, or positive.  Negative space is often viewed as the "background" whereas positive space is usually perceived as being in the "foreground."</p>
    </div>
    <img src="ryrie_building.jpg" alt="2-point perspective drawing of the ryrie building, perspective of south and west fascades">
    <div class="credit">
      [Burke, Horwood and White, Architects, 2013]
    </div>

    <div class="text">
      <h2 id="value">Value</h2>
      <p>Value is an aspect of color that describes lightness or darkness, and the difference between values is called value contrast.  By adding white to a color, we lighten it, creating a tint; and by adding black, we darken it, creating a shade.  By adding gray, we can create what's called a tone, and that's usually a good idea since pure colors are very bright.</p>
    </div>
    <div class="color-row">
      <ColorSquare color="hsl(180, 80%, 10%)" />
      <ColorSquare color="hsl(180, 80%, 20%)" />
      <ColorSquare color="hsl(180, 80%, 30%)" />
      <ColorSquare color="hsl(180, 80%, 40%)" />
      <ColorSquare color="hsl(180, 80%, 50%)" />
      <ColorSquare color="hsl(180, 80%, 60%)" />
      <ColorSquare color="hsl(180, 80%, 70%)" />
      <ColorSquare color="hsl(180, 80%, 80%)" />
      <ColorSquare color="hsl(180, 80%, 90%)" />
    </div>
    <div class="credit">
      [Lea Kapp, 2023]
    </div>

    <div class="text">
      <h2 id="color">Color</h2>
      <p>Color is probably one of the first words taught in the English language, yet it's difficult to define in words.  On a physical level, color is a certain type of reflecting into your eyes, but to define color as such misses the point entirely.  Colors instantly communicate messages on a deep psychological level.  To this day, I've never been able to explain color better than this video.  It reads like an ad for a particular pair of glasses, but the reaction is genuine.</p>
    </div>
    <div class="iframe-wrapper">
      <iframe src="https://www.youtube-nocookie.com/embed/WCcxwieuDH0" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
    </div>
    <div class="credit">
      [@EZwithETHAN, 2015]
    </div>
    
    <div class="text">
      <h1 id="principles-of-design">Principles of Design</h1>
      <p>Now that we know the elements of design, we can focus on how to use them effectively.  Obviously, we can't just splash a fistful of colors, lines, and shapes onto a pallet and call it art (unless you're Jackson Pollock).  We normies have to apply these elements in particular ways to achieve certain artistic effects.  The principles of design serve as guidelines that describe exactly how to do that.</p>
      <p>These principles include:</p>
      <ul>
        <li>Balance</li>
        <li>Repetition, Rhythm, and Pattern</li>
        <li>Emphasis and Contrast</li>
        <li>Proportion</li>
        <li>Movement</li>
        <li>Unity</li>
      </ul>
    </div>

    <div class="text">
      <h2 id="balance">Balance</h2>
      <p>Balance is the feeling of equality of visual weight within a composition across either side of an axis.  Visual weight is a broad topic in itself, but it refers to how "heavy" objects, colors, textures, and space "feel" when you perceive them.</p>
      <p>When either side of the composition uses the same characteristics, it's called symmetrical balance, and when either side uses different but equally weighted features, it's considered asymmetrical balance.  Finally, when the composition is entirely balanced both horizontally and vertically, we call that radial balance.</p>
    </div>
    <img src="last_supper.jpg" alt="leonardo da vinci's last supper">
    <div class="credit">
      [Leonardo da Vinci, 1498]
    </div>

    <div class="text">
      <h2 id="repetition-rhythm-pattern">Repetition, Rhythm, and Pattern</h2>
      <p>Repetition, rhythm, and pattern can be considered separate elements, but I think they're closely related enough to group them together.  Repetition is the easiest to define, as it's simply using either the same or very similar elements multiple times throughout the work.  By repeating these elements, we can create a pattern, but only if the repetition is structured rather than haphazard.  Finally, patterns establish the "rhythm" of the work, which creates a feeling or organized movement and unity that can help establish the mood for a work.</p>
    </div>
    <div class="color-row">
      <ColorSquare color="hsl(270, 80%, 25%)" />
      <ColorSquare color="hsl(270, 80%, 75%)" />
      <ColorSquare color="hsl(270, 80%, 25%)" />
      <ColorSquare color="hsl(270, 80%, 75%)" />
      <ColorSquare color="hsl(270, 80%, 25%)" />
      <ColorSquare color="hsl(270, 80%, 75%)" />
      <ColorSquare color="hsl(270, 80%, 25%)" />
      <ColorSquare color="hsl(270, 80%, 75%)" />
    </div>
    <div class="color-row">
      <ColorSquare color="hsl(270, 80%, 75%)" />
      <ColorSquare color="hsl(270, 80%, 25%)" />
      <ColorSquare color="hsl(270, 80%, 75%)" />
      <ColorSquare color="hsl(270, 80%, 25%)" />
      <ColorSquare color="hsl(270, 80%, 75%)" />
      <ColorSquare color="hsl(270, 80%, 25%)" />
      <ColorSquare color="hsl(270, 80%, 75%)" />
      <ColorSquare color="hsl(270, 80%, 25%)" />
    </div>
    <div class="color-row">
      <ColorSquare color="hsl(270, 80%, 25%)" />
      <ColorSquare color="hsl(270, 80%, 75%)" />
      <ColorSquare color="hsl(270, 80%, 25%)" />
      <ColorSquare color="hsl(270, 80%, 75%)" />
      <ColorSquare color="hsl(270, 80%, 25%)" />
      <ColorSquare color="hsl(270, 80%, 75%)" />
      <ColorSquare color="hsl(270, 80%, 25%)" />
      <ColorSquare color="hsl(270, 80%, 75%)" />
    </div>
    <div class="color-row">
      <ColorSquare color="hsl(270, 80%, 75%)" />
      <ColorSquare color="hsl(270, 80%, 25%)" />
      <ColorSquare color="hsl(270, 80%, 75%)" />
      <ColorSquare color="hsl(270, 80%, 25%)" />
      <ColorSquare color="hsl(270, 80%, 75%)" />
      <ColorSquare color="hsl(270, 80%, 25%)" />
      <ColorSquare color="hsl(270, 80%, 75%)" />
      <ColorSquare color="hsl(270, 80%, 25%)" />
    </div>
    <div class="color-row">
      <ColorSquare color="hsl(270, 80%, 25%)" />
      <ColorSquare color="hsl(270, 80%, 75%)" />
      <ColorSquare color="hsl(270, 80%, 25%)" />
      <ColorSquare color="hsl(270, 80%, 75%)" />
      <ColorSquare color="hsl(270, 80%, 25%)" />
      <ColorSquare color="hsl(270, 80%, 75%)" />
      <ColorSquare color="hsl(270, 80%, 25%)" />
      <ColorSquare color="hsl(270, 80%, 75%)" />
    </div>
    <div class="color-row">
      <ColorSquare color="hsl(270, 80%, 75%)" />
      <ColorSquare color="hsl(270, 80%, 25%)" />
      <ColorSquare color="hsl(270, 80%, 75%)" />
      <ColorSquare color="hsl(270, 80%, 25%)" />
      <ColorSquare color="hsl(270, 80%, 75%)" />
      <ColorSquare color="hsl(270, 80%, 25%)" />
      <ColorSquare color="hsl(270, 80%, 75%)" />
      <ColorSquare color="hsl(270, 80%, 25%)" />
    </div>
    <div class="credit">
      [Lea Kapp, 2023]
    </div>

    <div class="text">
      <h2 id="emphasis-contrast">Emphasis and Contrast</h2>
      <p>Once again, emphasis and contrast are closely related, but they are not the same thing.  Contrast is simply the arrangement of opposing elements within a composition, and it's usually used to create visual interest.  Light vs dark, rough vs smooth, etc.  However, contrast is often used to create emphasis, which is the art of directing the viewer's attention to a particular piece of the work.  Emphasis can also be created via use of isolation or visual economy.</p>
    </div>
    <img src="ai_lofi_girl.jpg" alt="an anime-style girl studying at her desk doing homework">
    <div class="credit">
      [<a href="https://www.freepik.com/free-ai-image/cartoon-lofi-young-manga-style-girl-studying-while-listening-music-raining-street-ai-generative_43227423.htm#query=digital%20art&position=1&from_view=search&track=ais">Image By chandlervid85</a>]
    </div>

    <div class="text">
      <h2 id="proportion-scale">Proportion and Scale</h2>
      <p>Proportion and scale are actually two words for the same thing:  the relative size among objects.  Scale can be used to create depth by making figures in the background smaller than images in the foreground, but it can also simply emphasize the bigger element.  Also important to the concept of proportion is the sense that the elements fit together.  Since we have a variety of canvas sizes in web design, dependent upon screen sizes, we need to ensure that our HTML elements can scale flexibly across various devices.</p>
      <p>This website was designed with a "mobile first" strategy using CSS breakpoints to shift certain elements dependent upon screen sizes.  Try opening it on a tablet or a phone, and you'll see that the proportions shift depending upon the layout.</p>
    </div>

    <div class="text">
      <h2 id="movement">Movement</h2>
      <p>Movement is a little confusing nowadays because modern art is frequently animated.  When you add the dimension of time to an art piece, literal movement becomes possible, but in the context of the principles of design, we aren't talking about the art moving.  Instead, in this context, movement refers to the path that the viewer's eye takes through the composition.  Movement is typically directed via lines, edges, shapes, and colors.</p>
    </div>
    <img class="white-background" src="arrows.png" alt="a series of arrows pointing left">
    <div class="credit">
      [HiClipart, Undated]
    </div>

    <div class="text">
      <h2 id="unity">Unity</h2>
      <p>Unity is found within the relationship between the parts and the whole.  When the elements within a composition are unified, they look like they belong together, like they compliment each other and the composition as a whole.  They reinforce the same themes and motifs.  Unity is fairly abstract, but you know it when you see it.</p>
    </div>
    <img src="circle_of_circles.webp" alt="9 photos of circular objects (some of which are arranged in a circle) arranged into a 3x3 grid pattern, forming a square">
    <div class="credit">
      [Lea Kapp, 2023]
    </div>

    <div class="text">
      <h1 id="rgb-color-theory">Bonus: RGB Color Theory</h1>
      <p>According to physics, what we see as color is the byproduct of neurons firing into the biochemical-electrical soup that is the human brain in response to your retinas coming in contact with electromagnetic waves of varying wavelengths within the spectrum of 430 to 790 terahertz.  In order from lower frequency to higher frequency:</p>
    </div>
    <img class="white-background" src="linear_visible_spectrum.svg" alt="depiction of the visible light spectrum">
    <div class="credit">
      [Wikipedia, 2008]
    </div>
    <div class="text">
     <p>The human eye has specialized cells called cones that are located in the retina.  Each cone specializes in detecting colors within a certain range of frequencies, and those frequencies are broken down into three categories:  red, green, and blue.  Since the cones do accept a range of frequencies, certain colors will have some overlap in the cones that they stimulate to different levels, and this allows us to distinguish even the smallest variations of color.</p>
     <p>Nowadays, most production model screens mix light using RGB color channels at a size of 8 bits, meaning that each pixel has an option of 24 bits worth of colors, or 24 ^ 2 = 16,777,216 colors to choose from.  Using CSS notation, we have access to this full range of color.  That might sound like a lot, and that's because it is.  The difference between these colors is almost imperceptible.</p>
     <p>Believe it or not, this is ten different colors:</p>
    </div>
    <div class="color-row">
      {#each countdown(128, 118) as hue}
        <ColorSquare color="rgb({hue}, 0, 255)" />
      {/each}
    </div>
    <div class="credit">
      [Lea Kapp, 2023]
    </div>

    <div class="text">
      <h2 id="color-wheel">Color Wheel</h2>
      <p>Isaac Newton first created the RYB color wheel by looking at a prism, realizing that light was composed of parts, and putting those colors in a circle.  Serendipitously, it lined up with knowledge of pigment mixing (RYB color wheel), and I guess that's fine and all, but if my wheel doesn't contain cyan and magenta, I will literally freak out.</p>
      <p>As such, my preferred wheel is RGB version:</p>
    </div>
    <img src="rgb_color_wheel.svg" alt="the rgb color wheel">
    <div class="credit">
      [Wikipedia, 2008]
    </div>

    <div class="text">
      <h2 id="color-mixing">Color Mixing</h2>
      <p>To mix colors, we specify how much red, green, and blue we want on a scale of 0-255.  Why 0-255?  Remember when I said each color has a channel of 8 bits?  8^2 = 256, so that's how much red, green, and blue we have to work with.  When you crank one of these up to 255 and set the rest to 0, you get the primary colors:</p>
      <ul>
        <li>Red</li>
        <li>Green</li>
        <li>Blue</li>
      </ul>
      <p>If you set two colors to 255 and the other to 0, you get the secondary colors:</p>
      <ul>
        <li>Yellow = red + green</li>
        <li>Cyan = green + blue</li>
        <li>Magenta = red + blue</li>
      </ul>
      <p>Finally, for tertiary colors, we can't actually add more of one color since we're already at the max.  Instead, we have to turn one of the colors down to the half-way point, 128.  To determine which color to reduce, it's helpful to consult the RGB color wheel.  Start with the secondary color that's closest to the tertiary color you're looking for, then move toward the desired color.  The primary color that you move toward should be set to 255, and the primary color you move away from should be set to 128.</p>
      <p>Or you could consult this list:</p>
      <ul>
        <li>Orange = red + ½ green</li>
        <li>Chartreuse = green + ½ red</li>
        <li>Rose = red + ½ blue</li>
        <li>Violet = blue + ½ red</li>
        <li>Azure = blue + ½ green</li>
        <li>Spring green = green + ½ blue</li>
      </ul>
      <p>Unfortunately, these colors aren't so good to work with unless you plan on blinding someone, so you'll almost always want to desaturate them.  Since desaturation requires some complicated math, I recommend HSL notation.  HSL stands for Hue, Saturation, and Lightness (value), and you can set each of these values individually.  Hue refers to the color, as measured by an angle around a circular color wheel.</p>
      <p>But that's a different class.</p>
    </div>
  </main>
</div>

<style>
  :global(body) {
    margin: 0px;
    font-family: "Fira Sans";
    box-sizing: border-box;
    background-color: hsl(240, 30%, 15%);
    color: hsl(0, 0%, 90%);
  }
  .container {
    display: grid;
    grid-template-areas:
      "nav"
      "main";
  }
  @media only screen and (min-width: 520px) {
    .container {
      grid-template-columns: 1fr 520px 1fr;
      grid-template-areas:
      "nav nav nav"
      "left main right";
    }
  }
  
  @media only screen and (min-width: 800px) {
    .container {
      grid-template-columns: 280px 2fr minmax(520px, 660px) 3fr;
      grid-template-areas:
      "nav left main right";
    }
    nav {
      top: 0;
      max-height: 100vh;
      overflow-y: auto;
      position: sticky;
    }
    nav > button {
      display: none;
    }
  }

  button {
    display: block;
    width: 100%;
    background-image: linear-gradient(hsl(210, 40%, 8%), hsl(210, 40%, 10%), hsl(210, 40%, 8%));
    color: hsl(210, 90%, 90%);
    border: none;
    font-size: 1.5em;
    font-weight: bold;
    padding-top: .3em;
    padding-bottom: .3em;
  }

  nav {
    grid-area: nav;
    display: block;
    font-size: 1.2em;
    font-weight: bold;
    /* transition: height .5s; */
  }
  nav ul {
    padding-left: 0;
  }
  nav li {
    padding-top: .6em;
    padding-bottom: .6em;
  }
  nav a {
    display: block;
    color: hsl(210, 90%, 90%);
  }
  nav a:visited {
    color: hsl(180, 90%, 90%);
  }
  nav a:hover {
    color: hsl(195, 80%, 90%);
  }
  
  nav > div > ul {
    margin-top: 0;
    margin-bottom: 0;
  }
  nav > div > ul > a {
    /* background-image: linear-gradient(hsl(210, 40%, 18%), hsl(210, 40%, 20%), hsl(210, 40%, 18%)); */
    background-color: hsl(210, 40%, 20%);
  }
  nav > div > ul > a:hover {
    /* background-image: linear-gradient(hsl(210, 40%, 70%), hsl(210, 40%, 80%), hsl(210, 40%, 70%)); */
    background-color: hsl(210, 40%, 80%);
    color: hsl(0, 0%, 5%)
  }
  nav > div > ul > a > li {
    display: block;
    padding-left: 1em;
    padding-right: 1em;
  }
  nav > div > ul > ul > a {
    /* background-image: linear-gradient(hsl(210, 40%, 22%), hsl(210, 40%, 24%), hsl(210, 40%, 22%)); */
    background-color: hsl(210, 40%, 24%);
  }
  nav > div > ul > ul > a:hover {
    /* background-image: linear-gradient(hsl(210, 40%, 70%), hsl(210, 40%, 85%), hsl(210, 40%, 70%)); */
    background-color: hsl(210, 40%, 85%);
    color: hsl(0, 0%, 5%)
  }
  nav > div > ul > ul > a > li {
    display: block;
    padding-left: 2em;
    padding-right: 1em;
  }

  main {
    grid-area: main;
    box-sizing: border-box;
    background-color:hsl(240, 30%, 10%);
  }

  a {
    color: hsl(210, 90%, 50%);
    text-decoration: none;
    scroll-behavior: smooth;
  }
  a:visited {
    color: hsl(180, 90%, 40%);
  }
  a:hover {
    color: hsl(195, 80%, 80%);
  }

  .color-row {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
  }

  h1 {
    font-size: 2.5em;
    letter-spacing: -2%;
    margin-top: 3em;
    margin-bottom: 1em;
    text-align: center;
    padding-left: 1em;
    padding-right: 1em;
  }
  h2 {
    font-size: 1.8em;
    letter-spacing: -1%;
    margin-top: 1.8em;
    margin-bottom: -.2em;
    text-align: center;
  }
  p {
    line-height: 1.5em;
    padding-top: .6em;
  }
  .text {
    padding-left: 1em;
    padding-right: 1em;
  }
  .credit {
    text-align: center;
    padding-top: 3px;
  }
  .bold {
    font-weight: bold;
  }

  img {
    width: 100%;
  }
  .white-background {
    background-color: hsl(0, 0%, 90%);
  }
  .iframe-wrapper {
    position: relative;
    box-sizing: content-box;
    padding-bottom: 56.25%; /* 16:9 aspect ratio */
  }
  .iframe-wrapper iframe {
    box-sizing: content-box;
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
  }

</style>