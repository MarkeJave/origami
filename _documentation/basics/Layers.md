---
title: Layers
layout: documentation
css: /public/css/documentation.css
weight: 1
nav:
  prev:
    label: Introduction
    path: ../index
  next:
    label: Interactions
    path: Interactions
---

[Layers](../patches/Layer.html) help draw to the viewer. They work like layers in Sketch and Photoshop: every layer has style attributes (e.g. position, size, an Image or Color to show...), can be different types (see list below), and can be layered on top of each other.

Add a layer with the patch library <span class="key modifier inline">&#8984;</span><span class="key letter inline">&#9166;</span>, or their [keyboard shortcuts](../workflow/KeyboardShortcuts.html).

## Layer patches
  <ul class="bulleted-list">
    <li>
      [Layer &rarr;](../patches/Layer.html) <span class="key letter inline">L</span>
      <br>
      Display a rectangle or image. For non-rectangle shapes, use patches like Circle Image or Rounded Rectangle that create an image to plug into a Layer.
      <br><br>
      In most situations, you'll be working with an image from your designs by copy-pasting or drag-and-dropping into the editor. This will automatically create a layer patch for you with the image connected.
    </li>
    <li>
      [Text Layer &rarr;](../patches/Text-Layer.html) <span class="key modifier inline">&#8679;</span><span class="key letter inline">T</span>
      <br>
      Display text with adjustable font settings.
    </li>
    <li>
      [Fill Layer &rarr;](../patches/Fill-Layer.html)
      <br>
      Completely fill the containing Layer Group with a color. Similar to paint bucket in Photoshop.
    </li>
  </ul>
## Layer position
Layers in Origami are positioned relative to the center of the viewer by default, where the center of the viewer is (x: 0, y: 0). You can change the Anchor Position from center to top left, but be aware most patches (like Scroll) expect Layers to remain centered.

<div class="coord-example">
  <div class="dot dot-center dot-center-y dot-center-x"></div>
  <div class="label dot-center dot-center-y dot-center-x">0, 0</div>

  <div class="dot dot-top-right dot-top dot-right"></div>
  <div class="label dot-top-right dot-top dot-right">150, 200</div>

  <div class="dot dot-bottom-left dot-bottom dot-left"></div>
  <div class="label dot-bottom-left dot-bottom dot-left">-150, -200</div>
</div>

X Position behaves like Sketch/Photoshop, where increasing it moves right, and decreasing moves left. Y Position, however, behaves differently: increasing it moves up, and decreasing moves down.

Read more about the [Coordinate System](../concepts/Coordinates.html).

## Layer order
Unlike the other attributes of a Layer, the order is determined with a dropdown at the top right of the Patch (instead of with an input). You can also change the order by selecting the layer and hitting <span class="key modifier inline">&#8984;</span><span class="key letter inline">[</span> or <span class="key modifier inline">&#8984;</span><span class="key letter inline">]</span>.

To dynamically change the order of a Layer, simply tweak the Z Position by a fraction (e.g. +/-0.0001).

## Layer Groups
[Layer Groups](../patches/Layer-Group.html) help you organize your Layers together. Create one from the patch library or simply hit <span class="key letter inline">G</span> (tip: hover over an image patch to group that image and inherit its size). You can double-click or <span class="key modifier inline">&#8984;</span><span class="key letter inline">&#9660;</span> to get into a Layer Group, and click **Edit Parent** in the toolbar or <span class="key modifier inline">&#8984;</span><span class="key letter inline">&#9650;</span> to exit a Layer Group.