<h1 align="center">Alicia Sykes - CV</h1>
<p align="center">
<!-- <a href="https://github.com/Lissy93/cv"><img src="https://i.ibb.co/8BV5p7L/CV-Logo-Alicia-Sykes.png" width="128" /><br /></a> -->
<i>This repo contains the source for my personal CV</i>
<br />
<b>🌐 <a href="https://cv.aliciasykes.com/">cv.aliciasykes.com</a> | 📄 <a href="https://cv.aliciasykes.com/download"><code>Alicia-Sykes-CV.pdf</code></a></b> <br />
</p>
<br />




> **Backstory**<br>
> I've just been made redundant 😢 (Aug '24), which I am gutted about. I've never been laid off before, and I loved my job and the people I worked with. So I'm now on the market, looking for a new role!
>
> I've kept my CV/resume **very** brief, in an attempt respect the hiring manager's time. But in short, I'm an experienced, Principle-level full stack engineer with a love for quality, performance, mentoring, tech and open source. The best judge of a developer is their code, and while I cannot share what I've done professional or for private clients, I have got many open source projects on my [GitHub](https://github.com/lissy93) and at [apps.aliciasykes.com](https://apps.aliciasykes.com).

---

## About

The resume content is defined in [`resume.yml`](/resume.yml) following the [jsonresume.org](https://jsonresume.org/) standard, and validated against [`schema.json`](/schema.json).
A LaTex document is then generated from [`template.jinja`](/template.jinja) formated with [`resume-format.cls`](/tex/resume-format.cls), which is then compiled into a PDF by GitHub Actions, and published under the [Releases](https://github.com/Lissy93/cv/releases) tab.
A markdown version is also generated by [`lib/markdown.py`](/lib/markdown.py), as well as a CV website which is built as a static Svelte site and deployed to GitHub Pages at [cv.aliciasykes.com](https://aliciasykes.com).<br>
...Because why spend 30 minutes writing your CV, when you could spend 30 hours automating it?


---

## Usage

### Option #1 - GitHub
Upon creating a tag (by triggering the [Tag Workflow](/.github/workflows/tag.yml)), a new Release will be drafted with your compiled CV PDF attatched

1. Fork the repo
2. Update resume.json with your own content
3. Trigger the GitHub Action to compile the PDF


<details><summary>Workflows</summary>

- `tag` - Creates a new Git tag. Optionally specify the tag name and description, or by default it will just bump the sem ver patch number by 1
- `generate` - Generates your resume in PDF form as an artifact. If triggered by a tag, then a new release will be created, with the PDF attatched
- `validate` - Validates your resume data against the schema. This will also run whenever a new PR is opened, to ensure it's valid and working 
</details>

---

### Option #2 - Local
See the [`Makefile`](/Makefile) for all the available commands. Or, just run `make` from the root, to install deps, validate content, generate LaTex, and compile PDF

1. Clone the repo
2. Update resume.json with your own content
3. Run `make` from the root, to install deps, validate content, generate LaTex, and compile PDF

<details><summary>Commands</summary>

- `make install` - Download dependencies
- `make validate` - Validate content
- `make generate` - Generate LaTex
- `make compile` - Compile PDF
- `make clean` - Remove generated files
- `make watch` - Watch for changes, recompile and refresh
- `make web` - Launches web version, installs NPM deps, builds and serves the site
</details>

---

### Editing
Modify data by editing [`resume.yml`](/resume.yml)<br>
If you need to customize the layout, edit [`template.jinja`](/template.jinja)<br>
Or to change the styles and formatting, edit [`resume-format.cls`](/tex/resume-format.cls)<br>
All the scripts used to generate output are located in [`lib/`](/lib/)<br>
These are triggered either by the [`Makefile`](/Makefile) or via GitHub Actions with the [`workflows/`](/.github/workflows)<br>
The source for the website version is located in [`web/`](/web)

---

## Screenshot

<p align="center"><a href="https://cv.aliciasykes.com"><img width="650" src="https://i.ibb.co/7NjgmHC/alicia-sykes-cv-mockup.png?" /></a></p>

---
  

## Attributions

### Contributors

![Contributors](https://readme-contribs.as93.net/contributors/lissy93/cv)

### Sponsors

![Sponsors](https://readme-contribs.as93.net/sponsors/lissy93)

---

## License

> _**[Lissy93/CV](https://github.com/Lissy93/cv)** is licensed under [MIT](https://github.com/Lissy93/cv/blob/HEAD/LICENSE) © [Alicia Sykes](https://aliciasykes.com) 2024._<br>
> <sup align="right">For information, see <a href="https://tldrlegal.com/license/mit-license">TLDR Legal > MIT</a></sup>

<details>
<summary>Expand License</summary>

```
The MIT License (MIT)

Copyright (c) Alicia Sykes <alicia@omg.com> 
Additional modifications Copyright (c) Scott Kirvan <hello@scottkirvan.com> 

Permission is hereby granted, free of charge, to any person obtaining a copy 
of this software and associated documentation files (the "Software"), to deal 
in the Software without restriction, including without limitation the rights 
to use, copy, modify, merge, publish, distribute, sub-license, and/or sell 
copies of the Software, and to permit persons to whom the Software is furnished 
to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included install 
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED,
INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANT ABILITY, FITNESS FOR A
PARTICULAR PURPOSE AND NON INFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT
HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION
OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE
SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
```

</details>

<!-- License + Copyright -->
<p  align="center">
  <i>© <a href="https://aliciasykes.com">Alicia Sykes</a> 2024</i><br>
  <i>Licensed under <a href="https://gist.github.com/Lissy93/143d2ee01ccc5c052a17">MIT</a></i><br>
  <a href="https://github.com/lissy93"><img src="https://i.ibb.co/4KtpYxb/octocat-clean-mini.png" /></a><br>
  <sup>Thanks for visiting :)</sup>
</p>

<!-- Dinosaur -->
<!-- 
                        . - ~ ~ ~ - .
      ..     _      .-~               ~-.
     //|     \ `..~                      `.
    || |      }  }              /       \  \
(\   \\ \~^..'                 |         }  \
 \`.-~  o      /       }       |        /    \
 (__          |       /        |       /      `.
  `- - ~ ~ -._|      /_ - ~ ~ ^|      /- _      `.
              |     /          |     /     ~-.     ~- _
              |_____|          |_____|         ~ - . _ _~_-_
-->

