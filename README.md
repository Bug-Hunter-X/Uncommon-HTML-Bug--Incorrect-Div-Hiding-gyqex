# Uncommon HTML Bug: Incorrect Div Hiding

This repository demonstrates a subtle bug in HTML related to CSS selectors. The code attempts to hide a specific div with the id "myDiv", but due to an incorrect selector, it may unexpectedly hide other divs on the page.

## Bug Description

The issue lies in using `document.querySelector('div')` to select the div element. This selector selects the *first* div element found in the document, regardless of its ID or other attributes. If the document contains multiple divs, the code will hide the first one instead of the intended target.

## Bug Solution

The correct way to hide the specific div is to use a more precise selector that targets the element by its ID, like `document.getElementById('myDiv')`.