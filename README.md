<br />
<div align="center">
  <p align="center">
    <a href="https://davidcetinkaya.github.io/embla-carousel" target="_blank"><img width="80" height="80" src="https://rawgit.com/davidcetinkaya/embla-carousel/master/docs/assets/embla-logo.svg" alt="Embla Carousel">
    </a>
  </p>

  <p align="center">
    <a href="https://opensource.org/licenses/MIT" target="_blank"><img src="https://img.shields.io/badge/license-MIT-green.svg"></a>
    <a href="https://www.npmjs.com/package/embla-carousel-react" target="_blank"><img src="https://img.shields.io/npm/v/embla-carousel-react.svg"></a>
    <a href="https://travis-ci.org/davidcetinkaya/embla-carousel-react" target="_blank"><img src="https://img.shields.io/travis/davidcetinkaya/embla-carousel-react/master.svg"></a>
    <a href="https://prettier.io" target="_blank"><img src="https://img.shields.io/badge/code_style-prettier-ff69b4.svg?style=flat"></a>
    <a href="https://www.npmjs.com/package/embla-carousel-react" target="_blank"><img src="https://img.shields.io/bundlephobia/minzip/embla-carousel-react?color=%234c1&label=gzip%20size">
    </a>
  </p>

  <strong>
    <h2 align="center">Embla Carousel React</h2>
  </strong>

  <p align="center">
    A tiny React.js wrapper for <a href="https://github.com/davidcetinkaya/embla-carousel">Embla Carousel</a>. Please visit the vanilla JavaScript <a href="https://github.com/davidcetinkaya/embla-carousel">package on Github</a> for documentation, available API methods and customizable options.
  </p>

  <br>

  <p align="center">
    <strong>
      <code>&nbsp;<a href="https://davidcetinkaya.github.io/embla-carousel">TRY DEMO</a>&nbsp;</code>
    </strong>
  </p>

  <br>

  <p align="center">
    <strong>
      <a href="#usage">usage</a>
      &nbsp; &middot; &nbsp;
      <a href="#props">props</a>
      &nbsp; &middot; &nbsp;
      <a href="#codesandbox">codesandbox</a>
    </strong>
  </p>

  <br>

  <p align="center">
    <a href="https://github.com/davidcetinkaya/embla-carousel">
      <img src="https://rawgit.com/davidcetinkaya/embla-carousel/master/docs/assets/javascript-logo.svg" height="45" alt="JavaScript" />
    </a>
    &nbsp;
    <a href="https://github.com/davidcetinkaya/embla-carousel-react">
      <img src="https://rawgit.com/davidcetinkaya/embla-carousel/master/docs/assets/react-logo.svg" height="45" alt="React" />
    </a>
  </p>
</div>
<br />

## Installation

NPM

<pre>npm install <a href="https://www.npmjs.com/package/embla-carousel-react">embla-carousel-react</a></pre>

## Usage

React Hooks

```javascript
import React, { useState, useEffect } from 'react'
import EmblaCarouselReact from 'embla-carousel-react'

const EmblaCarouselComponent = () => {
  const [embla, setEmbla] = useState(null)

  useEffect(() => {
    if (embla) {
      embla.on('select', () => {
        console.log(`Current index is ${embla.selectedScrollSnap()}`)
      })
    }
  }, [embla])

  return (
    <>
      <EmblaCarouselReact
        emblaRef={setEmbla}
        options={{ loop: false }}
      >
        <div style={{ display: 'flex' }}>
          <div style={{ flex: '0 0 100%' }}>Slide 1</div>
          <div style={{ flex: '0 0 100%' }}>Slide 2</div>
          <div style={{ flex: '0 0 100%' }}>Slide 3</div>
        </div>
      </EmblaCarouselReact>
      <button onClick={() => embla.scrollPrev()}>Prev</button>
      <button onClick={() => embla.scrollNext()}>Next</button>
    </>
  )
}

export default EmblaCarouselComponent
```

React Class

```javascript
import React, { Component } from 'react'
import EmblaCarouselReact from 'embla-carousel-react'

class EmblaCarouselComponent extends Component {
  componentDidMount() {
    this.embla.on('select', () => {
      console.log(
        `Current index is ${this.embla.selectedScrollSnap()}`,
      )
    })
  }

  render() {
    return (
      <>
        <EmblaCarouselReact
          emblaRef={c => (this.embla = c)}
          options={{ loop: false }}
        >
          <div style={{ display: 'flex' }}>
            <div style={{ flex: '0 0 100%' }}>Slide 1</div>
            <div style={{ flex: '0 0 100%' }}>Slide 2</div>
            <div style={{ flex: '0 0 100%' }}>Slide 3</div>
          </div>
        </EmblaCarouselReact>
        <button onClick={() => this.embla.scrollPrev()}>Prev</button>
        <button onClick={() => this.embla.scrollNext()}>Next</button>
      </>
    )
  }
}

export default EmblaCarouselComponent
```

## Props

- **`htmlTagName`** - Any valid HTML tag like `div` or `ul` etc.
- **`className`** - Applied to top the top level wrapper.
- **`emblaRef`** - Like a ref function to access the Embla instance in parent component.
- **`options`** - Same [options](https://github.com/davidcetinkaya/embla-carousel#options) as the vanilla JS Embla package.

## CodeSandbox

<p>Get started instantly with one of the CodeSandboxes below.</p>

<p>
  <img src="https://rawgit.com/davidcetinkaya/embla-carousel/master/docs/assets/codesandbox-logo.svg" height="23" align="top" alt="Embla Carousel CodeSandbox" /> &nbsp;
  <a href="https://codesandbox.io/s/embla-carousel-react-znjzv">
    <code>Basic Setup</code>
  </a> 
  - With Previous, Next & Dot buttons.
</p>

<p>
  <img src="https://rawgit.com/davidcetinkaya/embla-carousel/master/docs/assets/codesandbox-logo.svg" height="23" align="top" alt="Embla Carousel CodeSandbox" /> &nbsp;
  <a href="https://codesandbox.io/s/embla-carousel-react-iox4t">
    <code>Autoplay</code>
  </a> 
  - Example of how to setup Autoplay.
</p>

<br>
<br>

<h2 align="center">Open Source</h2>

<p align="center">
  <sup>Copyright © 2019-present, David Cetinkaya.</sup><br>
  Embla is <a href="https://github.com/davidcetinkaya/embla-carousel-react/blob/master/LICENSE">MIT licensed</a> 💖
</p>

<p align="center">
  <strong>· · ·</strong>
</p>

<p align="center">
  <a href="https://www.browserstack.com">
    <img src="https://rawgit.com/davidcetinkaya/embla-carousel/master/docs/assets/browserstack-logo.svg" height="60" alt="Embla Carousel BrowserStack" />
    </a>
</p>
