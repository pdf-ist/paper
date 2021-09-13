# 🌐📄 Paper

## 📏 [`size.css`](//open.pdf.ist/paper/size/)

### Demo

* https://open.pdf.ist/paper/size/

[![size.css](https://user-images.githubusercontent.com/27027/133064911-97187ace-5662-422a-a07e-79e15a7455b0.png)](//open.pdf.ist/paper/size/)


### Usage

* [codepen 👇🏻](//codepen.io/webpdf/pen/OJggOwa?editors=1000)

```HTML
<link href=//open.pdf.ist/paper/size.css rel=stylesheet>
<style>
  [size] {
    /*                                                            A4    letter
      --u:  paper size        unit                                 1mm     1in
      --w:  paper width                                          210       8.5
      --wu: paper width   ×   unit == calc(var(--w) * var(--u))  210mm     8.5in
      --h:  paper height                                         297      11
      --hu: paper height  ×   unit == calc(var(--h) * var(--u))  297mm    11in
    */
    aspect-ratio: var(--w) / var(--h); width: var(--wu);
  }
  .paper { background-color: #fbfbf8; outline: 1px solid #ccc; }
</style>
<div size=A4     class=paper></div>
<div size=letter class=paper></div>
```

### URLs

* https://open.pdf.ist/paper/size.css (📦 minified, recommended)
* https://cdn.jsdelivr.net/gh/pdf-ist/paper@latest/size.css (alternative)


---

# 💴 Sponsorship

This project is proudly sponsored by

| [`<pdf-page>`](//WebPDF.pro) |
| :-: |
| [<img src="https://webpdf.pro/.svg" width="64">](//WebPDF.pro) |
| [Web**PDF**.*pro*](//WebPDF.pro) |
