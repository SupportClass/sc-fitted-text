# \<sc-fitted-text\> [![Published on webcomponents.org](https://img.shields.io/badge/webcomponents.org-published-blue.svg)](https://www.webcomponents.org/element/SupportClass/sc-fitted-text) [![Build Status](https://travis-ci.org/SupportClass/sc-fitted-text.svg?branch=master)](https://travis-ci.org/SupportClass/sc-fitted-text) [![Coverage Status](https://coveralls.io/repos/github/SupportClass/sc-fitted-text/badge.svg?branch=master)](https://coveralls.io/github/SupportClass/sc-fitted-text?branch=master) ![Polymer 2 only](https://img.shields.io/badge/Polymer%202-only-blue.svg)

A Polymer 2 element for horizontally squishing text to stay within a max width.

## Motivation
Broadcast graphics often need to ensure that text will fit within a given space. There are existing libraries out there that can reduce the font size of an element to fit a given space, but this behavior isn't always what is wanted. Sometimes, the design calls for horizontally squishing (scaling) the text, rather than reducing the font size. This element enables that.

## Installation
```bash
bower install --save SupportClass/sc-fitted-text
```

## Example
<!--
```
<custom-element-demo>
  <template>
    <script src="../webcomponentsjs/webcomponents-lite.js"></script>
    <link rel="import" href="../web-animations-js/web-animations-next-lite.min.html">
    
    <link rel="import" href="../iron-demo-helpers/demo-pages-shared-styles.html">
    <link rel="import" href="../iron-demo-helpers/demo-snippet.html">
    <link rel="import" href="../iron-flex-layout/iron-flex-layout-classes.html">
    <link rel="import" href="../paper-dropdown-menu/paper-dropdown-menu.html">
    <link rel="import" href="../paper-input/paper-input.html">
    <link rel="import" href="../paper-item/paper-item.html">
    <link rel="import" href="../paper-listbox/paper-listbox.html">
    <link rel="import" href="../paper-slider/paper-slider.html">
    <link rel="import" href="../polymer/lib/elements/dom-bind.html">
    <link rel="import" href="sc-fitted-text.html">
    
    <custom-style>
      <style include="demo-pages-shared-styles iron-flex iron-flex-alignment">
        pre {
          display: inline;
        }
      </style>
    </custom-style>
    
    <dom-bind id="scope">
      <template is="dom-bind">
        <style>
          #fittedText {
            display: flex;
            height: 116px;
            align-items: center;
          }
        </style>
    
        <sc-fitted-text id="fittedText" text="[[text]]" max-width="[[maxWidth]]" align="[[align]]"></sc-fitted-text>
    
        <paper-input label="Text" value="{{text}}"></paper-input>
    
        <div class="layout horizontal end">
          <div>
            <label for="maxWidth">Max Width (0 to disable)</label>
            <paper-slider id="maxWidth" min="0" max="500" immediate-value="{{maxWidth}}" pin></paper-slider>
          </div>
    
          <div>
            <label for="fontSize">Font Size (in <pre>px</pre>)</label>
            <paper-slider id="fontSize" min="0" max="100" pin></paper-slider>
          </div>
    
          <paper-dropdown-menu label="Alignment">
            <paper-listbox slot="dropdown-content" attr-for-selected="value" selected="{{align}}">
              <paper-item value="left">Left</paper-item>
              <paper-item value="center">Center</paper-item>
              <paper-item value="right">Right</paper-item>
            </paper-listbox>
          </paper-dropdown-menu>
        </div>
      </template>
    </dom-bind>
    
    <script>
      const scope = document.getElementById('scope');
      scope.text = 'Hello world!';
      scope.maxWidth = 250;
      scope.align = 'left';
    
      const fittedText = document.getElementById('fittedText');
      const fontSize = document.getElementById('fontSize');
      fontSize.value = 14;
      fontSize.addEventListener('immediate-value-changed', e => {
        fittedText.style.fontSize = `${e.detail.value}px`;
        fittedText.fit();
      });
    </script>
  </template>
</custom-element-demo>
```
-->
```html
<sc-fitted-text text="Hello world!" max-width="100" align="center"></sc-fitted-text>
```

See the [Demo](https://www.webcomponents.org/element/SupportClass/sc-fitted-text/demo/demo/index.html) page for an interactive example.
