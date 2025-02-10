# Uncommon HTML Bug: Incorrectly Changing Text Content of a Div Element

This repository demonstrates a subtle bug that can occur when manipulating the content of HTML elements, specifically divs, using JavaScript. The issue arises when attempting to replace the existing content of a div that contains HTML tags.

## The Bug

The `textContent` property in JavaScript is intended to only get the plain text content of an element; it does not interpret or render any HTML tags within it.  When you use `textContent` to set new content within a div which already has other HTML elements inside it, it removes those other tags and replaces the content with plain text only. This usually isn't what a developer intended. 

The correct approach is to use `innerHTML`, which will correctly replace the content while also interpreting and rendering any HTML tags present.

## The Solution

The solution is simple: instead of using `textContent`, use `innerHTML`.  This will correctly replace the content of the div while preserving any nested HTML elements or handling new HTML being added.

## How to reproduce the bug
1. Open `bug.html` in your web browser.
2. Observe that the text within the div does not update correctly because textContent is used. 
3. Open `bugSolution.html` to see the corrected version. 