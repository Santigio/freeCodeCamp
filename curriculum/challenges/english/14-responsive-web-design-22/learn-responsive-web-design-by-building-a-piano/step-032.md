---
id: 612ec19d5268da7074941f84
title: Step 32
challengeType: 0
dashedName: step-32
---

# --description--

Add another `@media` rule to apply if the browser window is bigger than `769px` but smaller than `1199px`.

# --hints--

You should add a new `@media` query.

```js
assert(new __helpers.CSSHelp(document).getCSSRules('media')?.length === 2);
```

Your `@media` query should have a `min-width` of `769px` and a `max-width` of `1199px`.

```js
const mediaText = new __helpers.CSSHelp(document).getCSSRules('media')[1]?.media?.mediaText;
assert(mediaText === '(max-width: 1199px) and (min-width: 769px)' || mediaText === '(min-width: 769px) and (max-width: 1199px)');
```


# --seed--

## --seed-contents--

```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="UTF-8" />
    <title>Responsive Web Design Piano</title>
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <link rel="stylesheet" href="./styles.css">
  </head>
  <body>
    <div id="piano">
      <img class="logo" src="https://cdn.freecodecamp.org/platform/universal/fcc_primary.svg" alt="freeCodeCamp Logo" />
      <div class="keys">
        <div class="key"></div>
        <div class="key black--key"></div>
        <div class="key black--key"></div>
        <div class="key"></div>
        <div class="key black--key"></div>
        <div class="key black--key"></div>
        <div class="key black--key"></div>

        <div class="key"></div>
        <div class="key black--key"></div>
        <div class="key black--key"></div>
        <div class="key"></div>
        <div class="key black--key"></div>
        <div class="key black--key"></div>
        <div class="key black--key"></div>

        <div class="key"></div>
        <div class="key black--key"></div>
        <div class="key black--key"></div>
        <div class="key"></div>
        <div class="key black--key"></div>
        <div class="key black--key"></div>
        <div class="key black--key"></div>
      </div>
    </div>
  </body>
</html>
```

```css
html {
  box-sizing: border-box;
}

*, *::before, *::after {
  box-sizing: inherit;
}

#piano {
  background-color: #00471b;
  width: 992px;
  height: 290px;
  margin: 80px auto;
  padding: 90px 20px 0 20px;
  position: relative;
  border-radius: 10px;
}

.keys {
  background-color: #040404;
  width: 949px;
  height: 180px;
  padding-left: 2px;
  overflow: hidden;
}

.key {
  background-color: #ffffff;
  position: relative;
  width: 41px;
  height: 175px;
  margin: 2px;
  float: left;
  border-radius: 0 0 3px 3px;
}

.key.black--key::after {
  background-color: #1d1e22;
  content: "";
  position: absolute;
  left: -18px;
  width: 32px;
  height: 100px;
  border-radius: 0 0 3px 3px;
}

.logo {
  width: 200px;
  position: absolute;
  top: 23px;
}

@media (max-width: 768px) {
  #piano {
    width: 335px;
  }

  .keys {
    width: 318px;
  }

  .logo {
    width: 150px;
  }
}

--fcc-editable-region--

--fcc-editable-region--
```