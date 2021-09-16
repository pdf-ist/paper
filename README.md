# 🌐📄 paper

## 📏 [`size.css`](//open.pdf.ist/paper/size/)

* [**https://open.pdf.ist/paper/size/**](https://open.pdf.ist/paper/size/) ([👈🏻 **quick demo**](https://open.pdf.ist/paper/size/), utilizes [`aspect-ratio`](https://caniuse.com/mdn-css_properties_aspect-ratio))<br>([`aspect-ratio`](https://caniuse.com/mdn-css_properties_aspect-ratio) is [not really needed](#usage) but *makes sizing things a true breeze*™)<br><sub><sub><sub>(If your browser does not [support `aspect-ratio`](https://caniuse.com/mdn-css_properties_aspect-ratio) yet, see [**Usage**](#usage) section below for a simpler demo!)</sub></sub></sub>

```
(👇🏻 quick demo interactions legend 👇🏻)

on <pdf-page>
𝗰𝗹𝗶𝗰𝗸/𝘁𝗮𝗽: next page
𝗿𝗶𝗴𝗵𝘁-𝗰𝗹𝗶𝗰𝗸/𝗹𝗼𝗻𝗴-𝘁𝗮𝗽: previous page

on a paper size
𝗵𝗼𝘃𝗲𝗿 (🖱️ mouse): highlight size
𝗰𝗹𝗶𝗰𝗸/𝘁𝗮𝗽: overlay size on <pdf-page> and focus

anywhere
𝘁𝗮𝗯 (⌨️ key): switch focus between sizes
𝗲𝘀𝗰 (⌨️ key): cancel size overlay


(𝘐𝘧 𝘺𝘰𝘶 𝘥𝘰 𝘯𝘰𝘵 𝘴𝘦𝘦 𝘢𝘯𝘺𝘵𝘩𝘪𝘯𝘨, 𝘶𝘱𝘨𝘳𝘢𝘥𝘦 𝘺𝘰𝘶𝘳 𝘣𝘳𝘰𝘸𝘴𝘦𝘳...
𝘙𝘦𝘢𝘥 𝘮𝘰𝘳𝘦 𝘰𝘯 𝘵𝘩𝘪𝘴 𝘰𝘯 𝘵𝘩𝘦 𝘨𝘪𝘵𝘩𝘶𝘣 𝘱𝘢𝘨𝘦 𝘶𝘯𝘥𝘦𝘳 𝗦𝗲𝗲 𝗮𝗹𝘀𝗼!)
```

[![size.css](https://user-images.githubusercontent.com/27027/133064911-97187ace-5662-422a-a07e-79e15a7455b0.png)](//open.pdf.ist/paper/size/)


### Usage

* [codepen 👇🏻](//codepen.io/webpdf/pen/OJggOwa?editors=1000)

```HTML
<link href=//open.pdf.ist/paper/size.css rel=stylesheet>
<style>
  [size] {
    /*                                                         A4    letter
      --u:  paper   size   unit                                 1mm       1in
      --w:  paper  width                                      210         8.5
      --h:  paper height                                      297        11
      --wu: paper  width × unit == calc(var(--w) * var(--u))  210mm       8.5in
      --hu: paper height × unit == calc(var(--h) * var(--u))  297mm      11in
    */
    aspect-ratio: var(--w) / var(--h);
           width: var(--wu);
  }
  @supports not (aspect-ratio: 1 / 1) { [size] { height: var(--hu); } }  

  .paper { background-color: #fbfbf8; outline: 1px solid #ccc; }
  .paper[size=letter] { position: absolute; transform: translateY(-100%); }
  .paper:hover { opacity: .5; }
  .paper::before { content: attr(size); position: absolute; font-family: system-ui; }
</style>
<div size=A4     class=paper></div>
<div size=letter class=paper></div>
```

### URL

* [https://<u>open</u>.**PDF**.*ist*/paper/size.css](https://open.pdf.ist/paper/size.css) <br>(📦 minified, via ⛅ Cloudflare CDN)


### Series

```
ISO 4A0 2A0 A0→10 A2→5-extra A3→4-super super-A3→4 A4-long  ✔️
            B0→10   B5-extra                                ✔️
            C0→10   C7/6 DL                                 ✔️
JPN     JIS-B0→12                                           ✔️
CHN         D0→6                                            ✔️
           RD0→6                                            ✔️
USA letter legal ...                                        🚧
```

### See also

* https://caniuse.com/mdn-css_properties_aspect-ratio<br>not really needed but *makes sizing things a true breeze*™


---

# 💴 Sponsorship

This project is proudly sponsored by

| [`<pdf-page>`](//WebPDF.pro) |
| :-: |
| [<img src="https://webpdf.pro/.svg" width="64">](//WebPDF.pro) |
| [Web**PDF**.*pro*](//WebPDF.pro) |

#### [World's Best PDF Web Components](https://WebPDF.pro)

Professional PDF web components<br>
in the form of HTML custom elements

Now featuring WASM-powered<br>
[high-fidelity](https://github.com/pdf-ist/WebPDF/discussions) `♊ PDFium` rendering.
