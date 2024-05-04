# Frequently Used Class Names in HTML Markup

## Fork by ![**@LexPearson**](https://github.com/lexpearson) from ![**aleksanderlamkov/html-classnames**](https://github.com/aleksanderlamkov/html-classnames) <br><br>General Rules
- Avoid using numbers in class names.
    ```html
    <!-- ❌ Incorrect -->
    <div class="element-1">...</div>
    
    <!-- ✅ Correct -->
    <div class="first-element">...</div>
    ```
- Write class names in lowercase using `kebab-case` notation, where each word is separated by a hyphen.
    ```html
    <!-- ❌ Incorrect -->
    <div class="userinfo">...</div>
    <div class="Userinfo">...</div>
    <div class="userInfo">...</div>
    <div class="UserInfo">...</div>
    <div class="USERINFO">...</div>
    <div class="USER-INFO">...</div>
    <div class="USER_INFO">...</div>

    <!-- ✅ Correct -->
    <div class="user-info">...</div>
    ```
- Class names should not consist of a single letter.
    ```html
    <!-- ❌ Incorrect -->
    <div class="w">...</div>

    <!-- ✅ Correct -->
    <div class="wrapper">...</div>
    ```
- Avoid excessive abbreviations in class names; use `button` instead of `btn` and `link` instead of `lnk`. Remember, code is written once, but read by you and other developers much more often, so saving characters is not advisable.
    ```html
    <!-- ❌ Incorrect -->
    <button class="btn">...</button>
    <a class="lnk">...</a>

    <!-- ✅ Correct -->
    <button class="button">...</button>
    <a class="link">...</a>
    ```
- In most cases, class names should not duplicate the tag name of the element to which the class is applied.
    ```html
    <!-- ❌ Incorrect -->
    <p class="p">...</p>
    <div class="div">...</div>
    <a class="a">...</a>

    <!-- ✅ Correct -->
    <p class="paragraph">...</p>
    <div class="wrapper">...</div>
    <a class="link">...</a>
    ```
- Class names should generally reflect the function or style of the element.
    ```html
    <!-- ❌ Incorrect -->
    <button class="some-button">Red Button</button>
    <div class="some-block">Tooltip</div>

    <!-- ✅ Correct -->
    <button class="red-button">Red Button</button>
    <div class="tooltip">Tooltip</div>
    ```
- Class names can consist of multiple words; however, it is logical that the fewer words in a class name, the easier it is to write, read, and remember.
    ```html
    <!-- ✅ Acceptable -->
    <span class="user-name-first-letter">A</span>
    ```
- In class names, you can and should combine words if the context of the element requires it (e.g., a block with the class `user` may contain blocks with the classes `user-image` and `user-name`, and `user-name` may contain an element with the class `user-name-first-letter`).
    ```html
    <!-- ✅ Correct -->
    <div class="user">
      <img class="user-image" />
      <div class="user-name">
        <span class="user-name-first-letter">A</span>lexander
      </div>
    </div>
    ```
- Often, it's better to use nouns for class names, and in rare cases, adjectives when the class serves as a modifier of a component. Verbs are generally not used as class names.
    ```html
    <!-- ❌ Incorrect -->
    <a class="go-back">...</a>
    <button class="submit">...</button>
    <form class="create-user">...</form>
    <div class="run-slider">...</div>

    <!-- ✅ Correct -->
    <a class="go-back-link">...</a>
    <button class="submit-button">...</button>
    <form class="create-user-form">...</form>
    <div class="slider">...</div>

    <!-- ⚠️ Also Correct -->
    <button class="button red wide bold">...</button>
    <section class="section large-padding-y">...</section>
    ```
- Every class in the project should be justified. For example, if you have 5 sections that are absolutely identical in style but have different content, there is no need to invent a separate class for each section; it's better to use a unified class.
    ```html
    <!-- ❌ Incorrect -->
    <section class="banner">...</section>
    <section class="features">...</section>
    <section class="catalog">...</section>
    <section class="about">...</section>
    <section class="contacts">...</section>
    <style>
      .banner { padding-block: 30px }
      .features { padding-block: 30px }
      .catalog { padding-block: 30px }
      .about { padding-block: 30px }
      .contacts { padding-block: 30px }
    </style>

    <!-- ✅ Correct -->
    <section class="section">...</section>
    <section class="section">...</section>
    <section class="section">...</section>
    <section class="section">...</section>
    <section class="section">...</section>
    <style>
      .section { padding-block: 30px }
    </style>
    ```

## Structural Blocks with Semantic Tags
- `page` — `<html>` or `<body>`
- `header` — `<header>`
- `content`, `main` — `<main>`
- `footer` — `<footer>`
- `section` — `<section>`
- `aside`, `sidebar`, `widget`
— `<aside>`
- `nav`, `menu`, `navigation` — `<nav>`

## Structural Blocks with Neutral Tags (div, span)
- `inner`, `body` — auxiliary element
- `wrapper`, `wrap` — auxiliary wrapper element
- `container` — container limiting the width of the content
- `grid` — table-like grid
- `row` — row in a grid
- `column`, `col`, `cel` — column (cell) in a grid

## Lists
- `list`, `items` — `<ul>`, `<ol>`, and `<dl>` elements
- `item` — `<li>` element

## Cards
- `card` — `<article>` element

## Images
- `image`
- `img`
- `picture`
- `pic`
- `thumbnail`
- `thumb`
- `avatar`
- `logo`
- `icon`

## Text
- `title`, `subtitle`, `heading`, `subheading`, `headline`, `subject`, `caption`, `label` — elements from `<h1>` to `<h6>`
- `slogan`, `description`, `text` — slogans and descriptions
- `blockquote`, `quote` — quotes
- `copyright` — copyright
- `link` — links
- `code`, `snippet` — code snippets

## Forms
- `form` — `<form>` element
- `form-group` — `<fieldset>` element
- `form-group-name`, `form-group-title`, `form-group-label` — `<legend>` element
- `form-item` — structural form element wrapping input elements

## Classic Input Fields
- `field` — root `<div>` element of an input field component
- `field-label` — `<label>` element
- `field-control` — `<input />`, `<textarea>`, `<select>` elements

## Checkboxes
- `checkbox` — root `<label>` element of a checkbox component
- `checkbox-control` — `<input />` element of a checkbox component
- `checkbox-emulator` — `<span>` element of a checkbox component for emulating the "square"
- `checkbox-label` — `<span>` element of a checkbox component for labeling

## Radio Buttons
- `radios` — root `<fieldset>` element of a radio button component
- `radios-label` — `<legend>` element of a radio button component

## Miscellaneous
- `button` — `<button>` element
- `dropdown` — dropdown list
- `accordion`, `spoiler` — accordion component
- `modal`, `popup` — modal window
- `overlay`, `backdrop` — darkening background (e.g., behind modal windows)
- `tooltip`, `hint` — tooltip, popup hint
- `slider`, `carousel` — slider
- `pagination` — pagination (horizontal menu with page numbers and left-right arrows)
- `breadcrumbs` — breadcrumb navigation (hierarchical navigation of a web application, often following the header)
- `basket`, `cart` — shopping cart
- `summary`, `total`, `amount` — sum of something (e.g., total order amount)
- `search`, `quick-search` — search form
- `user` — element with user data
- `features`, `advantages`, `benefits` — element with a list of product or service features
- `socials`, `soc1als` — social networks

## Size Modifiers
- `small`
- `tiny`
- `medium`
- `base`
- `big`
- `large`
- `huge`
- `narrow`
- `wide`

## Presence Modifiers
- `has-icon`
- `has-error`
- `has-underline`

## State Modifiers
- `is-current` — current menu item
- `is-active` — active button
- `is-visible`, `is-shown` — visible tooltip
- `is-hidden`, `hidden` — hidden information
- `is-open` — open modal window
- `is-expanded` — expanded dropdown list
- `is-invalid`, `is-error` — input field with incorrect input data
- `warning` — warning
- `alert`, `notification` — notification
- `success` — success status of something
- `loading`, `processing`, `pending` — loading status
