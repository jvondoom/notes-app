# Memorandum

## Purpose
This is the log of the decision making during the development of this app.

## Methodology
This document will follow the Quaestio structure taken from the Summa Theologiae of Thomas Aquinas, which is build in the following way:
### **Date - Question**

**Objections**
- Example of a point

**Sed contra** (counter-statement)
- Example of a counter-statement for the previous point

**Answer**
Considering the objections and the counter-statements, we provide an answer to the Quaestio bringed.

---

## Dev Log

### Why using a single file instead of separating the UI, the code, and the styles?
**Objections**
- Best practices recommend to keep a file for the UI, another for the styles, and a separated one for the functionality.

**Sed Contra**
- Even though following the best practices is the default recommendation, every single project is unique and the requirements dictate if is valid to make an exception of the best practices

**Answer**
The original solution his application resolved does not had a regular deployment environment where a regular solution could be executed, therefore this app required to be created in a single HTML file.

---

### 11/16/2026 - Should the buttons be wrapped in a div?
**Objections**
- Extra div elements should not be used.
- Additional code will be written to add the buttons into the wrapper

**Sed Contra**
- Extra div elements should not be added to the DOM, unless they are needed to achieve a better UI/UX
- Additional code can be written in a separate function which the solely purpose to handle that.

**Answer**
In order to allow the UI to present the created buttons in any design, the `loadView` function will create a div element to parent all the buttons, which can be stylized later using the class `button-wrapper`.
