# Memorandum

## Purpose
This is the log of the decision making during the development of this app.

## Methodology
This document will follow the Quaestio structure taken from the Summa Theologiae of Thomas Aquinas, which is build in the following way:
- **Date - Question**
- **Objections**
- **Sed contra** (counter-statement)
- **Answer**

## Dev Log

### 11/16/2026 - Should the buttons be wrapped in a div?
**Objections**
- Extra div elements should not be used.
- Additional code will be written to add the buttons into the wrapper

**Sed Contra**
- Extra div elements should not be added to the DOM, unless they are needed to achieve a better UI/UX
- Additional code can be written in a separate function which the solely purpose to handle that.

**Answer**
In order to allow the UI to present the created buttons in any design, the `loadView` function will create a div element to parent all the buttons, which can be stylized later using the class `button-wrapper`.
