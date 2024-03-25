# Tanedo Group Website 2024

Hosted at  [particle.ucr.edu](https://particle.ucr.edu)

Flip Tanedo
March 2024

Please consider [sponsoring the creator](https://github.com/sponsors/gcushen) if you use Hugoblox. 

I periodically re-do my personal website from scratch using the latest Academic template. Most of the material in this document copied from earlier websites. This `README.md` file is a personal reminder of how I edited the page. 

Old versions:  [2023](https://github.com/fliptanedo/FlipWebsite2023)| [2022](https://github.com/fliptanedo/FlipWebsite2022/blob/main/README.md) | [2021](https://github.com/fliptanedo/tanedo-website-2021/blob/master/README.md) | [2020](https://github.com/fliptanedo/flip-www-2020)

Here's what the 2023 version looked like:

![image-20240325103923449](/Users/fliptanedo/Documents/Website/FlipWebsite2024/figures/image-20240325103923449.png)

## Quick Start from Scratch

I do not use the Netlify-based default deployment.

1. Use the Wowchemy [Academic Resumé template](https://github.com/wowchemy/starter-hugo-academic); there is a green button to `use this template` that will create a repository on your GitHub account.
   ![UseThisTemplate](/Users/fliptanedo/Documents/Website/FlipWebsite2024/figures/UseThisTemplate.png)

2. Pull the code locally, e.g. `Code` > `GitHub CLI` 
   ![Screenshot 2024-03-25 at 10.35.39 AM](/Users/fliptanedo/Documents/Website/FlipWebsite2024/figures/Screenshot 2024-03-25 at 10.35.39 AM.png)

3. Start hacking the template by copying over bits from the old site. (I started with this `README.md` file.) The steps for this are summarized below. As you go through this, update the `README.md` file accordingly. You future self will thank you (take this moment to thank me).

4. Make sure you have Hugo e.g. through Homebrew. If it's been a while, you may want to update (up**grade**) hugo using `brew upgrade hugo` at the terminal. 

   `hugo server -D` 

   The output will include a URL: `Web Server is available at http://localhost:1313/`, navigate your browser to this URL to view the page. [Link for convenience](http://localhost:1313/).

5. Copy over `.gitignore` from the previous version. Start a new `README.md` file (I save the Wowchemy readme as a different filename). Push to GitHub.

6. Clean up/back up the default Wowchemy page. 

   1. Make a backup copy of `./content/_index.md` ; this controls the home page widgets.
   2. Open `./content/_index.md` and delete most of the sections other than the first `about.biography`. For reference, the `markdown` block is the default no-frills block. 
   3. Remove the extraneous items in `./config/_default/menus.yaml` (everything but the `Home` item)
   4. `/config/_default/params.yaml`
      1. `# SEO`: empty out everything
      2. `# Site header`: align right, turn off day/night, search
      3. `# site features`: 
      4. Copy over `## ADDED BY FLIP` parameters from 2022 page
   5. `./config/config.yaml`: copy over modifications from 2022 page

7. Update `./content/authors/admin/_index.md` ; copy from 2022 page. Copy `avatar.jpg` from here too. I added a line `pronouns: he/him` in `./content/authors/admin/_index.md`; may want to use this in the future.

8. Prepare a `layouts_templates` folder. Refer to the [Hugo Blox: Extend Hugo Blox documentation](https://docs.hugoblox.com/reference/extend/#override-a-component); you need to match the template to the module version; this is trivial if you're doing a fresh install. You'll need to download a local copy of [HugoBlox/hugo-blox-builder](HugoBlox/hugo-blox-builder) and copy the `/modules/blox-bootstrap/layouts` to a new `./layouts_templates` folder. Also make an empty-for-now `./layouts` folder. We will copy files from `layouts_templates` into `layouts` to overrwrite components as needed. Do the same for `./modules/blox-bootstrap/assets` and copy it into `./assets_templates` if you have to copy over and make custom `scss` or `js` code. Background: [Modifying Modules](https://gohugo.io/hugo-modules/use-modules/#make-and-test-changes-in-a-module)


## Useful References

* The [Hugo Directory Structure](https://gohugo.io/getting-started/directory-structure/): All paths are relative to the project root

* [Extending Hugo Blox](https://docs.hugoblox.com/reference/extend/)

  ```
  To override a template in the theme, you simply copy the file you are interested in from the version of the Wowchemy module your site uses and paste it in your site folder using a similar path. To choose your version, select its tag from GitHub’s dropdown master box on the upper left and press enter.
  ```

* [Hugo Blox Docs](https://docs.hugoblox.com)

* [Nick Ballou's customization page](https://nickballou.com/blog/custom-wowchemy/#add-background-image-to-bottom-of-about-widget)

* [hackmd.io](https://hackmd.io/@noisyoscillator/hugo-academic-customizations)

## What's changed since 2023?

Updates: Wowchemy is now known as HugoBlox. 

### Updates in HugoBlox

* There's a `./config/_default/hugo.yaml` file with some basic data. This includes the source structure for permalinks relative to the `./public/` folder. 

* There is more [documentation](https://docs.hugoblox.com/reference/extend/) for customizing the framework, including:  

  * how to use **hooks** to avoid having to hard-code templates.  There are hooks for the start/end of the header, the end of the body, the start of the footer.
    ```
    To inject your code into one of the above places, create a file at layouts/partials/hooks/<hook>/<your-filename>.html, replacing <hook> with one of the hook names above and <your-filename> with any name, such as custom. You’ll need to create these new folders relative to the root of your site.
    For example, to inject your code into the site head, you can create a file at layouts/partials/hooks/head-end/custom.html.
    You can have multiple files in each hook folder, with Hugo determining the order which they are rendered in.
    ```

  * Explicit instructions for overwriting components. This is what we used to call layout files. 

* HugoBlox offers Tailwind as an alternative to Bootstrap styling. I'm sticking to Bootstrap for now.

## Updates in my workflow

I have added a `./figures/` folder for images specifically for this `README.md` file. 

### Notes for this year and next

* I may want to properly upgrade my custom css to [scss](https://www.geeksforgeeks.org/what-is-the-difference-between-css-and-scss/).
* I want to embed my slides. I'm working on a reasonable way to do this. Google Slides perhaps? 
  * It looks like Bootstrap has a way to deal with embeds: https://getbootstrap.com/docs/4.0/utilities/embed/

* I backed up some old sites in `./static/archived/`. These show up under `./archived/` when uploaded. Should I link to them? These archived sites are a huge pain. They take up a large amount of space. I think it's from the saved pdfs of talks. I think there should be a better way of archiving these in the future.
* There are a bunch of image files that are much larger than they need to be. The media folder is around 50 mb. I should make small versions of the images.

* The hero block may be a nice way to put in the top watermark without having to hack the `baseof` template. Try this in `_index.md`:

  ```
  - block: hero
      id: test 
      content: 
        title: hi
        image:
          filename: hero-academic.png
  ```

  This gives a slight white "watermark". See these [instructions for section background](https://docs.hugoblox.com/tutorial/link-in-bio/step-4/).

* As I start writing up separate pages, I may want to work out a better file system for `./content/`. Most of my independent pages show up in `./content/posts/` and are otherwise unsorted. They get called by, for example:

  ```
  {{ $.Site.BaseURL }}img/portfolio/{{ .photo }}
  ```

  (from my design portfolio). 

* I had to remove the "recent talks" section from my landing page (homepage). This was mainly because the `<details>` tag seems to make slideshare embeds not load properly, but anyway the whole thing was kind of clunky. I've come around to the idea of using the Wowchemy "featured publications" or "projects" block for this. It's a little more work, but ultimately I think that's what I want to do. My research slider can link to a separate page.  

* It looks like the Hugo Blox hooks aren't quite in the places where I'd like them. However, one thing that I can do is to use those code snippits to create new hooks in the places where I want them. Is this worth it? Not in the immediate term. It mainly saves the trouble of editing the `baseof.html` file too much.

## Transferring Assets

All paths in this document are relative to the project root, `FlipWebsite2024/` 

### Copying Over Old Content

Unlike the 2022 version, Wowchemy no longer uses `./content/home`  for individual markdown files for each home page widget. Instead, all of this information goes into `./content/_index.md`. I copied over the old `./content/home` directory into `./content/home_OLD` for easy copy and pasting.

### Transferring Assets

#### Style Sheets

Adding custom style sheets: [[source](https://wowchemy.com/docs/hugo-tutorials/extending-wowchemy/)]

1. Create the `./assets/scss/` folder if it doesn’t exist
2. Create a file named `custom.scss` in the `./assets/scss/` folder
3. Add your custom CSS code to the file you created and re-run Hugo to view changes

We just copy over the folder from `./assets/` in the 2023 version.

#### Media

1. Transfer over the favicon, `./assets/media/icon.png`. [[source](https://docs.hugoblox.com/getting-started/customize/#website-icon)] This should be a 512x512 px image.
2. Transfer over the `./assets/photos/` folder. This is a good time to make sure none of the files are too big. 
3. Transfer over the `./assets/research/` folder. This is a good time to make sure none of the files are too big. 

### Shortcodes

Copy the files from `./layouts/shortcodes/`: `twitter.html` and `flipemail.html`

### More image and file assets

#### Static Folder

Transfer the `./static` folder. This one has lots of potentially large files. It is a good time to do housekeeping to remove anything that is no longer being used. 

#### Content

Transfer the folders from `./content/post` which contain the pages beyond the front page. I use these "blog posts" for my design portfolio.

### Fonts and color theme

Note: you can refer to [HugoBlox/hugo-blox-builder](HugoBlox/hugo-blox-builder) to see what the default theme and font files look like. For now they are still in toml rather than yaml.

Copy `./data/fonts/flipfont.toml`

Copy `./data/themes/fliptheme.toml`

 Choose a colour theme and font set in `config/_default/params.yaml`. 

```
appearance:
  # theme_day: minimal
  # theme_night: minimal
  theme_day: fliptheme
  font: flipfont
  # font: minimal
  font_size: L
```

One comment on `fliptheme.toml`: I found that the `primary` color is what ends up as the page background color when over-scrolling. (Below this comes up as "fixing the background color"). It turns out that after doing all my other hacks, `primary`  really just sets the over-scroll background color. My 2022 default had this over-scroll as green, which is a bit (unintentionally) bold stylistically. Instead, use `#333333` as a default. I do not think this affects anything else. Links are still in green, `#4caf50`. 

```
[light]
  # Primary
  # primary = "#4caf50"
  primary = "#333333"
```

* [Font instructions](https://wowchemy.com/docs/getting-started/customization/#custom-font)

* From the old [Wowchemy personalization page](https://wowchemy.com/docs/getting-started/customization/#fonts):

  > Otherwise, to force your visitors to see either a light or dark theme, set only a day *or* night theme, but *not* both.

  Comment out the `theme_night` option in `params.yaml`. This overrides the `show_day_night` toggle and forces the page to only give light mode. [New documentation](https://docs.hugoblox.com/getting-started/customize/#appearance).

## Checkpoint

At this point, you've transferred over most of the assets. This is a good time to push to commit and push to your main repo on GitHub to save your progress.

Here's what the page looks like right now: don't mind the fact that it's totally dark. Also don't mind that it takes Safari a while to update the favicon; in a pinch you can delete the favicon cache at `~/Library/Safari/Favicon Cache`. 

![Screenshot 2024-03-25 at 10.36.12 AM](/Users/fliptanedo/Documents/Website/FlipWebsite2024/figures/Screenshot 2024-03-25 at 10.36.12 AM.png)

Seriously, don't freak out about the background. Here's an explanation. At this point, the background color for odd-numbered setions is very dark. I believe this is just the background color that I set somewhere. This came from some hubris I had about editing `/layouts/_default/baseof.html`. Here's what I wrote in the 2021 version (edited)

> 1. **We want the *actual* background of `<body>` to be dark gray.** Aesthetically we want the background to be white. However, the navigation bar and footer will be dark gray. What this means is that if one over-scrolls (pulls above or below the main page by a little) then you get a bit of white pulling from under the footer or from above the navigation bar. This is distracting, so we're going to jump through some hoops. This involves:
>
>    a) setting the `<body>` background to be dark gray. If you've copied over the style files, this should already be active.
>
>    b) creating a new `<div id="THECONTENT">` that has a white background. All of the sections will be inside this division. Over scrolling, however, will pull more space from *outside* this division, which will be dark gray.
>
> 2. **We want the fancy footer**. I have a neat Feynman diagram footer graphic that I like.  Observe that the `<div class="container">` that encloses the footer does not spread across the entire navigator width.  The `container` class is something inherited from Bootstrap, the responsive design grid system that *Academic* is built upon.
>
>    We have to place additional `<div>`s just around and above the footer. 
>
>    Bonus: at this stage you can also put in the `baseof.html` code for a watermark.
>
>    In earlier steps we defined the locations of the graphics in `params.yaml`

The road in the past has been to hack  `./layouts/_default/baseof.html`. It would be nice if the Hugo Blox hooks can help here, but they do not seem to appear at quite the ideal places, so we'll continue the way we have before by hacking at templates. 

## Building up the framework

Pages follow the following overall template: `./layouts/_default/baseof.html`. Like all layout documents, the version in `./layouts_templates/` that we copied from the Hugo Blox GitHub repo is what the system defaults to. However, it will look in the `./layouts/` folder for any templates that should supercede the default. Thus, if you want to hack `baseof.html`, copy `./layouts_templates/_default/baseof.html` into  `./layouts/_default/baseof.html` and work on the latter.

### Baseof

Ok, time to hack  `./layouts/_default/baseof.html`. It's easiest to refer to the previous version to see where the edits are. Mark these with comments to make them really clear.

1. Vanity: add a comment at the top of the page to note that I've edited the Hugo Blox template. Insert into Line 3.
   ```html
   <!DOCTYPE html>
   {{ "<!-- This site was created with Hugo Blox. https://hugoblox.com -->" | safeHTML }}
   <!-- FLIP: added a little string in here -->
   {{ "<!-- Flip Tanedo has edited the Hugo Blox template.  -->" | safeHTML }}
   ```

2. Below the `{{ if .Params.announcement.text -}}` block, put in the watermark div, Line 37:

   ```html
    {{ if .Params.announcement.text -}}
       {{ partial "components/announcement_bar" . }}
     {{ end -}}
   
     <!-- FLIP: FOR WATERMARK -->
     <div id="watermark" style="background-image:url('{{ $.Site.BaseURL }}/img/{{ .Site.Params.watermark }}');"></div>
     <!-- /FLIP --> 
   ```

3. Below `{{/* Load header block */}}` and above `<div class="page-body">`, Line 54:

   ```html
     {{ partial $block_path . }}
     </div>
   
   <!-- FLIP: opened a new div id="THECONTENT" for framing -->
   <div id="THECONTENT">
   <!-- Closed below; see ./assets/scss/custom.css -->
   <!-- /FLIP -->
   
   
     <div class="page-body">
   ```

   Go ahead and close it just above `{{ partial "site_js" . }}`, Line 84:

   ```html
     <!-- FLIP -->
     </div> <!-- closes id="THECONTENT" -->
     <!-- /FLIP -->
   
     {{ partial "site_js" . }}
   ```

   1. Now backtrack and dig into `<div class="page-footer">`, insert the following after `{{ if not (in (slice "book" "docs" "updates") .Type) }}`; we're surrounding the `class="container"` div. Line 78:


   ```html
     <div class="page-footer">
       {{/* Docs and Updates layouts include the site footer in a different location. */}}
       {{ if not (in (slice "book" "docs" "updates") .Type) }}
       <!-- FLIP -->
       <div style="position: relative; width: 0; height: 0">
         <div id="feynmanfoot" style="background-image:url('{{ $.Site.BaseURL }}/img/{{ .Site.Params.footmark }}');"></div>
       </div>
       <div id="botbar1"></div>
         <!-- -- -->
       <div id="FOOTERBAR"> 
       <!-- closed after container -->
       <!-- /FLIP -->
       <div class="container">
         {{ partial "site_footer" . }}
       </div>
       <!-- FLIP -->
       </div> <!-- closes div FOOTERBAR -->
       <!-- /FLIP -->
       {{ end }}
     </div>
   ```

   At this point the page should render with all the appropriate components. The footer bar may need some height calibration.

#### Editing Footer CSS 

For 2024 I didn't need to futz with this.

1. Pop back into `./assets/scss/custom.scss`. We need to fiddle with the `top` padding on `#botbar1`: 

   ```
   	padding: 0;
     	position:relative;
     	top: 70px;
   ```

   That should set the horizontal line correctly. To move the Feynman diagram, modify `#feynmanfoot`. I found that a similar 70px shift works. The original value is `bottom: 160px;`, I moved it to:

   ```
   bottom: 90px;
   ```

2. There's one remaining oddity. The color of the "over scroll". In `./data/themes/fliptheme.toml` the `primary` color sets the "background" of the page.  To fix this, go to `fliptheme.toml` and create a new option: 

   ```
   [light]
     # Primary
     primary = "#4caf50"
     flip_bg = "#333333"
     # ... shows up when you "overscroll"
   ```

   Then go to (or copy and create) `./layouts/partials/functions/parse_theme.html` and under `{{/* Load Theme. */}}`, Line 57:

   ```html
   {{ if site.Params.appearance.theme_day }}
     <!-- FLIP EDIT -->
     <!-- {{- $scr.Set "primary" ($theme_day.primary | default "#1565c0") -}} -->
     {{- $scr.Set "primary" ($theme_day.flip_bg | default "#1565c0") -}}
     <!-- /FLIP EDIT -->
   ```

   

## Setting up the site

Any edits to templates that I make now are edits that I will need to make again in the future when doing my next major update. In order to document this, mark any edits  in templates with comments along the lines of `<!-- FLIP EDIT -->` and `<!-- /FLIP EDIT -->`. For simple edits no need to use the open/close. This makes it easy to search for edits. 

I don't want to simply copy my hacked templates into new versions of ~~Wowchemy~~ Hugo Blox because updates in ~~Wowchemy~~ Hugo Blox can dramatically change the inter-relationships of template files. It is much better to start from the most updated Wowchemy and make small perturbations on a working system.

## Two Column Block

The templates for blocks (previously known as widgets) live in `./layouts/partials/blocks/`. 

The blank template layout is  `./layouts/partials/blocks/markdown.html` (copy this from `./layouts_templates/...`). However, there's a caveat. At full width, we want our blocks to have two columns with the block title on the left and the block contents on the right. The default Wowchemy scheme only allows certain blocks to do this property. The relevant line in `./layouts/partials/functions/parse_block_v2.html` (copy it over if it's not already there) is the following around Line 98:

```
{{ $use_cols := in (slice "collection" "experience" "accomplishments" "contact" "markdown" "tag_cloud" "portfolio") $block_type }}
```

Only blocks with the listed tags are allowed to use the two-column mode. Examining `parse_block_v2.html`  you will find an `if $use_cols` statement that prints the title on the left-hand side subject to the bootstrap responsive design css. (Bootstrap is the framework that interprets classes like `col-12 col-lg-4 mb-3 mb-lg-0` into elements that resize when you change the window width.)

In order to get around this, we'll make our own two column widget template.

Make a copy of `./layout/partials/blocks/markdown.html` and call it `./layout/partials/blocks/fliptemplate.html`. (Or rename the copy of `markdown.html`)

* Add some commented text at the top explaining the new block. 
* Change the default number of columns to 2. 
* Now we add a chunk of text in the `{{ if ne $columns "1" }}` case that we can copy from `parse_block_v2.html` to render the left-hand column.

Here's what it looks like on my end:

```html
{{/* FLIP: new template block */}}
{{/* BASED ON: Hugo Blox: Markdown */}}
{{/* FLIP: use this for making new 2-col blocks */}}
{{/* Documentation: https://hugoblox.com/blocks/ */}}
{{/* License: https://github.com/HugoBlox/hugo-blox-builder/blob/main/LICENSE.md */}}
{{/* FLIP EDITS: the default markdown block template    */}}
{{/* has no explicit code for the left column.          */}}
{{/* This code is hidden in pase_block.html and         */}}
{{/* only accessible to the official blocks.            */}}


{{/* Initialise */}}
{{ $page := .wcPage }}
{{ $block := .wcBlock }}
<!-- FLIP: DEFAULT SET TO 2 -->
{{ $columns := $block.design.columns | default "2" }}
<!-- /FLIP -->
{{ $text := $block.content.text | emojify | $page.RenderString }}

<!-- FLIP: FROM parse_block_v2.html: OPEN DIV 1 -->
<div class="row  {{if not $block.content.title | or (eq $columns "1") }}justify-content-center{{end}}">
<!-- /FLIP EDIT -->

{{ if ne $columns "1" }}
<!-- FLIP EDIT: COPIED FROM parse_block_v2.html -->
    
  {{ if $block.content.title }}
    {{ if eq $columns "1" }}
      <div class="section-heading col-12 mb-3 text-center">
        {{ with $block.content.title }}<h1 class="mb-0">{{ . | markdownify | emojify }}</h1>{{ end }}
        {{ with $block.content.subtitle }}<p class="mt-1">{{ . | markdownify | emojify }}</p>{{ end }}
      </div>
    {{else}}
      <div class="section-heading col-12 col-lg-4 mb-3 mb-lg-0 d-flex flex-column align-items-center align-items-lg-start">
        {{ with $block.content.title }}<h1 class="mb-0">{{ . | markdownify | emojify }}</h1>{{ end }}
        {{ with $block.content.subtitle }}<p class="mt-1">{{ . | markdownify | emojify }}</p>{{ end }}
      </div>
    {{end}}
  {{end}}

<!-- /FLIP EDIT: COPIED FROM parse_block_v2.html -->
  <div class="col-12 col-lg-8">
    {{ $text }}
  </div>
{{ else }}
  <div class="col-12">
    {{ $text }}
  </div>
{{ end }}

<!-- FLIP EDIT: COPIED FROM parse_block_v2.html: CLOSE DIV 1 -->
</div>
<!-- /FLIP EDIT -->
```

Here's a good test for `./content/_index.md`; add the following to the `sections` list:

```yaml
  - block: fliptemplate
    id: test
    content:
      title: Test
      subtitle: test
      text: Some test words. Did you know that 
        you can spread the text out over multiple
        lines by using tabs?
    design:
      columns: '2'
```

### Navbar

The navbar defaults to a "large" menu. See `./layouts/partials/components/headers/navbar.html`. (Create this if needed, copying from `./layouts_templates`.) Changing the `nav` class to `navbar-expand-md` means the "hamburger" only shows up for small screens. 

```html
<header>
  <!-- FLIP: use navbar-expand-md; could even use navbar-expand-sm if short -->
  <nav class="navbar navbar-expand-md navbar-light compensate-for-scrollbar" id="navbar-main">
  <!-- <nav class="navbar navbar-expand-lg navbar-light compensate-for-scrollbar" id="navbar-main"> -->
  <!-- /FLIP -->
```

### Footer

The newest version of Wowchemy allows you to make a custom footer. These are stored in `./layouts/partials/components/footers`. The default footer is `minimal.html`.

Make a copy of `./layouts/partials/components/footers/minimal.html` and call it `flipfoot.html`. Go to `./config/_default/params.yaml` and use `flipfoot` as the block:

```
footer:
  block: flipfoot
  copyright:
    notice: '© {year} Me. This work is licensed under {license}'
    license:
      enable: true
      allow_derivatives: false
      share_alike: true
      allow_commercial: false
```

Now we can edit `flipfoot.html`.  Here's what I use:

```html
<div class="row" id="footer-columns">
  <div class="col-md-4" id="footer-col-1">
    <img src="{{ $.Site.BaseURL }}img/{{ $.Site.Params.mylogo }}" class="center-me">
  </div>
  <div class="col-md-4" id="footer-col-1">
    <!-- <img src="{{ $.Site.BaseURL }}img/{{ $.Site.Params.midlogo }}" class="center-me"> -->
    {{ with site.Params.footer.text }}
    <p class="powered-by">
      {{ . | markdownify | emojify }}
    </p>
    {{ end }}

    {{/* Display copyright license. */}}
    {{ partial "site_footer_license" . }}
  </div>
  <div class="col-md-4" id="footer-col-1">
    <p class="powered-by">
    {{ with site.Copyright }}{{ replace . "{year}" now.Year | markdownify}}{{ end }}

    {{ if ne .Type "docs" }}
    <span class="float-right" aria-hidden="true">
      <a href="#" id="back_to_top">
        <span class="button_icon">
          <i class="fas fa-chevron-up fa-2x"></i>
        </span>
      </a>
    </span>
    {{ end }}
  </p>
  </div>
</div>
```

Note: the copyright information is split between blocks in `./config/_default/params.yaml` and `./config/_default/hugo.yaml`. I may want to tweak that in the future so they're both in the same place.  For `hugo.yaml`  you have to add a `copyright` attribute:

```yaml
title: Flip Tanedo # Website name
baseURL: 'https://particle.ucr.edu/' # Website URL
## FLIP: new addition
copyright: 'Opinions on this site do not represent those of any other groups. Conversely, the policies of my university and funding agencies do not necessarily represent my values.'
```



# Content

We'll go down the list of homepage blocks. It is not worth describing the custom block modifications. These are all based on `./layouts/partials/blocks/fliptemplate.html` to have the nice two column layout. You'll need to make copies of `fliptemplate.html` for each modified block. 

Note: if `fliptemplate.html` (which was based on `markdown.html`) hasn't changed since the last revision, then you can just copy over the custom blocks from the previous version. I suggest going over the existing blocks and seeing how they are modified. I did not bother indicating where the edits are: they are all over the place and should be straightforward to follow.

**Remark:** the `./layouts/partials/blocks/fliptemplate.svelte.html` block is a version of `fliptemplate.html` that "knows" you have a two column layout and trims off the "if you want a one-column layout" code. I use this in some of the custom blocks.

Everything is updated in `_index.md` and with the menu updated in `menus.yaml`. In `_index.md` it is useful to know that `|-` means "markdown follows in the following line." For example:

```yaml
sections:
  - block: flip.avatar
    id: about
    content:
      title: 
      username: admin
      text:
      blurb: |-
        Flip is the first Filipino-American professor of particle physics. He runs a [Physical Science book club](https://sites.google.com/ucr.edu/physci-book-club/) (Phy-Sci) at his local independent book store. He enjoys swimming, basketball, and speculative fiction.
```



## About Block

This one requires quite a bit of work. The default `about.avatar.html`  assumes that you want a one column design. We'll hack pieces of that file into`fliptemplate.html` . Create a new "about" block called `flip.avatar.html` and call it in `_index.md`. 

There are quite a lot of changes, so suffice it to say that I should just copy `flip.avatar.html`. I made some minor edits to `custom.scss` (which should already have copied over). In `_index.md`:

```
sections:
  - block: flip.avatar
    id: about
    content:
      username: admin
      text:
      blurb: Flip is the first Filipino-American professor of particle physics. He runs a Physical Science book club (Phy-Sci) at his local independent book store. He enjoys swimming, basketball, and speculative fiction.
```

## CV

This is another one where one should just copy the `flip.cv.html` template. Note that the filenames should be in pure lowercase. 

The CV block is a nice demonstration for how to iterate over lists and sub-lists. Some care is necessary since Hugo is reading `_index.md` as a yaml file. You can use the `{{ . | markdownify }}` construction to apply markdown to an item, for example `{{ .thing | markdownify }}`. However, the `thing` cannot start out with markdown or else Hugo will get confused. Instead, you can use a single quote:

```
service:
      - thing: Website Committee (chair)
      - thing: '[hyperlink](https://www.google.com)'
```



## Slider (Carousel)

The slider/image carousel is tricky. At the time of this writing, the slider had not yet been ported to a v2 template, though GitHub user Agos95 [has a fix](https://github.com/wowchemy/wowchemy-hugo-themes/blob/3b417723f711d3fbb9392f5613fc7b91bebd53db/modules/wowchemy/layouts/partials/blocks/slider.html). It seems to work, so I advocate just grabbing it and placing it in `./layouts/partials/blocks/`.

Note: it is important that the slider template is called `slider.html`. Any other name (e.g. `flip.slider.html`) will not work because bits of code (e.g. `parse_block_v2.html`) specifically have `if` statements based on whether the  block is *exactly* `slider`.  See `parse_block_v2.html`:

```
{{/* Special case: Slider widget. */}}
{{ if in (slice "slider") $block_type }}
  {{ $css_classes = print $css_classes " carousel slide" }}
  {{ $extra_attributes = printf "data-ride=\"carousel\" data-interval=\"%s\"" (cond ($block.design.loop | default true) (string $block.design.interval | default "3000") "false") }}
  {{ $use_container = false }}
{{ end }}

```

Trying to recreate the slider block is a pain because it is hard to get the new block to span the entire width and height of a block... not to mention the bigger issue that the navigation does not work.

1. Download [this file](https://github.com/wowchemy/wowchemy-hugo-themes/blob/3b417723f711d3fbb9392f5613fc7b91bebd53db/modules/wowchemy/layouts/partials/blocks/slider.html) as `./layouts/partials/blocks/slider.html`. Hopefully in the future this will be part of the default Wowchemy blocks.
2. Copy over the `_index.md` lines. 

It turns out that it works great now. There were some tweaks for buttons. I'm not quite sure where these get set, but I'll just hack these by hand in `custom.scss`.



**References**

* [vw units](https://coderwall.com/p/hkgamw/creating-full-width-100-container-inside-fixed-width-container)
* [#2914 pull request](https://github.com/wowchemy/wowchemy-hugo-themes/pull/2914) and see also [2919](https://github.com/Agos95/wowchemy-hugo-themes/commit/f55ff594c0f63899a8af893f33bd62ceb77cc8fd)

## Students

The main edits to the `fliptemplate.html` file are in the second column:

```
<div class="col-12 col-lg-8">
  {{ $text }}

  {{ with $block.mygroup }}
    <ul class="ul-students">
      {{ range .students }}
        <li class="ul-students" title="{{ .name }}">
          <a href="{{ .website }}"><img class="studentpic" src="{{ $.Site.BaseURL }}img/students/{{ .photo }}"></a>
        </li>
      {{ end }}
    </ul>
  {{ end }}

  <p><span class="comment">* - co-advised,  ◊ - postdoc, † - undergraduate, ‡ - high-school, § - visiting</span></p>


  <div class="row comment">
    <h5>Past Students</h5>
  </div>

  {{ with $block.mygroup }}
    {{ range .oldstudents }}
      <div class="row comment">
        <div class="col-xs-3">
          <a href="{{ .website }}" class=comment>
            {{ .name }}&nbsp;
          </a>
        </div>
        <div class="col-xs-3">
          {{ .start }} - {{ .end }}&nbsp;
        </div>
        <div class="col-xs-6">
          {{ .position }}, {{ .role }}
        </div>
      </div>
    {{ end }}
  {{ end }}

</div>
```

## Twitter (Social Media)

This lightly edits the  `markdown` block. 

```
  <div class="col-12 col-lg-8">
    {{ $text }}
    <h4>Recent Press</h4>
    {{ if $block.content.currentpress }}
    <div>
      {{ $block.content.currentpress | markdownify }}
    </div>
    {{ end }}

    {{ if $block.content.olderpress }}
    <details>
      <summary><b>Older Press</b></summary>
      <div>
        {{ $block.content.olderpress | markdownify }}
      </div>
      {{ end }}
    </details>
  </div>
```



## Portfolio (Design)

These are all stored in `./contents/posts/`. Actually, all of my pages are stored in that folder, not just portfolio pages. In the future I may want to branch off and make a separate folder. 

Make a new template called `flip.portfolio.html`. 

## Contact

You can use the `contact` block, but I don't like how large the Font Awesome icons are. These, in turn, are tied to specific Wowchemy css that tunes the size of the height of the list items (`li`) to the Font Awesome 2x size.

We can make our own contact template, but we need to start with `fliptemplate.html` because Wowchemy defaults to only allowing two column view for a specific set of named blocks. That is: when we rename `contact` to `flip.contact` it stops rendering properly in at least two places: (1) the wide screen two column view does not work, (2) the height of the list items fails. 

You can find the css code for the list item heights in `_contact.scss`, which you can download from [Wowchemy](https://github.com/wowchemy/wowchemy-hugo-themes/tree/main/modules/wowchemy). Go to: `[downloadfolder]wowchemy-hugo-themes-main/modules/wowchemy/assets/scss/wowchemy`. The relevant chunk is here:

```
.wg-contact .fa-ul {
  margin-left: 3.14285714rem; /* Must be > `fa-2x` icon size. */
}

.wg-contact .fa-li {
  position: absolute;
  left: -3.14285714rem; /* Negative of `.wg-contact .fa-ul` margin. */
  width: 2rem; /* Match `fa-2x` icon size. */
  top: 0.14285714em; /* Default FA value. */
  text-align: center;
}

.wg-contact li {
  padding-top: 0.8rem; /* Align text with bottom of `fa-2x` icon. */
  margin-bottom: 0.3rem;
}
```

We'll use that as a reference. 

First we'll make a copy of `fliptemplate.html` (which is written to work in two-column mode) called `flip.contact` and then copy over bits and pieces from `contact.html`

Be sure to copy these two initializations from `contact.html`:

```
{{ $autolink := default true $block.content.autolink }}
{{ $data := $block.content }}
```

Here's my sloppy hack in `custom.scss`:

```
// contact, adapted from _contact.scss

.fa-ul {
  // margin-left: 3.14285714rem;
}

.fa-li {
  position: absolute;
  left: -3rem; /* Negative of `.wg-contact .fa-ul` margin. */
  width: 2rem; /* Match `fa-2x` icon size. */
  top: 0.14285714em; /* Default FA value. */
  text-align: center;
}
```

I hope that doesn't affect font awesome lists anywhere unexpected.

There were a bunch of little tweaks, this one is kind of fun.







## "Sponsors"

There's a lot of work one can do here. The sponsors are a list of graphics and widths:

```
sponsors:
      - sponsor: bob
        logo: logo_DOE.png
        logowidth: 1116
      - sponsor: bob
        logo: logo_NSF.png
        logowidth: 200
      - sponsor: bob
        logo: logo_Hellman.png
        logowidth: 541
    sponsorwidth: 28.57
```

`sponsorwidth` is just the sum of logo widths divided by 100, then add a little bit as a fudge factor.

# OLD: FLIP IS HERE



* 

# Deployment

The most straightforward deployment is to run `hugo` and then upload the `./public/` folder via SSH or SFTP. 

Wowchemy recommends deploying with Netlify: this syncs your local directory with GitHub, and then deploys the `./public/` folder to a netlify web address. I have found it tricky to figure ot how to sync my university address to the netlify web address. 

My current setup is that my university gives me web space on an AWS server. 

* To explore: I may be able to still [sync to GitHub with AWS](https://aws.amazon.com/blogs/devops/integrating-with-github-actions-ci-cd-pipeline-to-deploy-a-web-app-to-amazon-ec2/). [Tutorial from AWS](https://aws.amazon.com/getting-started/hands-on/host-static-website/).
* [2020 unofficial tutorial](https://samwelek.co.uk/2020/10/05/how-to-host-your-static-website-on-aws-with-github-actions/)

# Troubleshooting

[Wowchemy troubleshooting page](https://wowchemy.com/docs/hugo-tutorials/troubleshooting/).

* `Error: from config: failed to resolve output format "headers" from site config`
  * [Wowchemy docs on this](https://wowchemy.com/docs/hugo-tutorials/troubleshooting/#error-failed-to-resolve-output-format); for me `hugo mod clean --all` ended up solving the problem
  * Discussions: [GitHub](https://github.com/wowchemy/wowchemy-hugo-themes/discussions/2800), [Nov 2021](https://user.it.uu.se/~justin/Hugo/post/hugo_module_fail/), [in Mandarin](https://zenn.dev/meihei/articles/32bb275f71e938), [Hugo issue and CTA](https://github.com/gohugoio/hugo/issues/10208), 

# Misc Notes

It looks like one can use [hugo code in the css file](https://discourse.gohugo.io/t/how-to-use-hugo-template-variables-in-css/4464), though the source is old. (Update: [better discussion here](https://discourse.gohugo.io/t/trying-to-make-theme-colors-configurable-in-css-with-hugo-pipes-but-getting-a-css-syntax-error/26739); looks like the thing to search for is CSS and Hugo Pipes.)

* Some discussion about [lightmode/darkmode images](lightmode/darkmode images), including a nice hack for SVG images (of which I have none).
* Could also have two copies of the css file, one for light/dark. But now this doubles the work of updating the css. What would be better is if we used scss and had some Hugo code at the top that defines the colors. 
* Most likely I should leave this to a future revision. 
* Can probably use `invert()` to deal with images using css? See [this discussion](https://developer.mozilla.org/en-US/docs/Web/CSS/filter-function/invert). 

## People

This was an informative block from the 2022 Wowchemy Academic Resume templates. It seems to have gone away, but I'm reproducing it here because it looks informative.

```
{{/* Wowchemy Blocks: People */}}
{{/* Documentation: https://wowchemy.com/blocks/ */}}
{{/* License: https://github.com/wowchemy/wowchemy-hugo-themes/blob/main/LICENSE.md */}}

{{/* Initialise */}}
{{ $page := .wcPage }}
{{ $block := .wcBlock }}
{{ $show_social := $block.Params.design.show_social | default false }}
{{ $show_interests := $block.Params.design.show_interests | default true }}
{{ $show_organizations := $block.Params.design.show_organizations | default false }}
{{ $show_role := $block.Params.design.show_role | default true }}

<div class="row justify-content-center people-widget">
  {{ with $block.Title }}
  <div class="col-md-12 section-heading">
    <h1>{{ . | markdownify | emojify }}</h1>
    {{ if $block.Params.subtitle }}<p>{{ $block.Params.subtitle | markdownify | emojify }}</p>{{ end }}
  </div>
  {{ end }}

  {{ with $block.Content }}
  <div class="col-md-12">
    {{ . }}
  </div>
  {{ end }}

  {{ range $block.Params.content.user_groups }}
  {{ $query := where (where site.Pages "Section" "authors") ".Params.user_groups" "intersect" (slice .) }}

  {{if $query | and (gt (len $block.Params.content.user_groups) 1) }}
  <div class="col-md-12">
    <h2 class="mb-4">{{ . | markdownify }}</h2>
  </div>
  {{end}}

  {{ range $query }}
  {{ $avatar := (.Resources.ByType "image").GetMatch "*avatar*" }}
  {{/* Get link to user's profile page. */}}
  {{ $link := "" }}
  {{ with site.GetPage (printf "/authors/%s" (path.Base .File.Dir)) }}
    {{ $link = .RelPermalink }}
  {{ end }}
  <div class="col-12 col-sm-auto people-person">
    {{ $src := "" }}
    {{ if site.Params.features.avatar.gravatar }}
      {{ $src = printf "https://s.gravatar.com/avatar/%s?s=150" (md5 .Params.email) }}
    {{ else if $avatar }}
      {{ $avatar_image := $avatar.Fill "270x270 Center" }}
      {{ $src = $avatar_image.RelPermalink }}
    {{ end }}
    {{ if $src }}
      {{ $avatar_shape := site.Params.features.avatar.shape | default "circle" }}
      {{with $link}}<a href="{{.}}">{{end}}<img width="270" height="270" loading="lazy" class="avatar {{if eq $avatar_shape "square"}}avatar-square{{else}}avatar-circle{{end}}" src="{{ $src }}" alt="Avatar">{{if $link}}</a>{{end}}
    {{ end }}

    <div class="portrait-title">
      <h2>{{with $link}}<a href="{{.}}">{{end}}{{ .Title }}{{if $link}}</a>{{end}}</h2>
      {{ if and $show_organizations .Params.organizations }}{{ range .Params.organizations }}<h3>{{ .name }}</h3>{{ end }}{{ end }}
      {{ if and $show_role .Params.role }}<h3>{{ .Params.role | markdownify | emojify }}</h3>{{ end }}
      {{ if $show_social }}{{ partial "social_links" . }}{{ end }}
      {{ if and $show_interests .Params.interests }}<p class="people-interests">{{ delimit .Params.interests ", " | markdownify | emojify }}</p>{{ end }}
    </div>
  </div>
  {{ end }}
  {{ end }}
</div>

```

