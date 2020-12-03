---
layout: distill
title: Getting Started
description: instructions to add a blog post on this website
date: 2020-12-02

authors:
  - name: Wenxuan Zhou
    affiliations:
      name: Robotics Institute, Carnegie Mellon University

bibliography: 2018-12-22-distill.bib

---

## Getting Started

### Installations
- Install [Git](https://github.com/git-guides/install-git) and get familiar with the basic operations.
- This website is built using Jekyll. Follow the [instructions](https://jekyllrb.com/docs/installation/) to install all the dependencies to run Jekyll on your machine in order to visualize your post while editing.

### Run the website on your local machine
[Fork](https://docs.github.com/en/free-pro-team@latest/github/getting-started-with-github/fork-a-repo) the repository of [this website](https://github.com/Wenxuan-Zhou/robostats-wiki). 
Clone your version of this repository to your local machine and run it:

<d-code block language="shell">
git clone https://github.com:&lt;your-username&gt;/robostats-wiki.git
cd robostats-wiki
bundle install
bundle exec jekyll serve
</d-code>

There should be an instruction in the terminal saying:
<d-code block language="shell">
Server address: http://127.0.0.1:4000/robostats-wiki/
</d-code>

Now you can open `http://127.0.0.1:4000/robostats-wiki/` in your browser. This is a local version of the website on your machine.

### Create a new post
To create a new post, you will first copy the template. Make sure to name it in the format of `<year>-<month>-<date>-<title>.md`!

<d-code block language="shell">
cd robostats-wiki/_posts
cp 2020-12-02-instruction.md &lt;year&gt;-&lt;month&gt;-&lt;date&gt;-&lt;title&gt;.md 
</d-code>

If you refresh the local website `http://127.0.0.1:4000/robostats-wiki`, you will now find your post under the blog.
You can start editing the file `<year>-<month>-<date>-<title>.md` and check the format by refreshing the local website.

### Submission

After you finish editing the post, you can submit a [pull request](https://docs.github.com/en/free-pro-team@latest/github/collaborating-with-issues-and-pull-requests/creating-a-pull-request). 
Make sure to submit the pull request to `robostats-wiki` instead of the template of the website `al-folio`.
One of the TAs will process your pull request and publish your blog post on the website.

## Useful templates
Here are some useful elements that you might use in the blog post.

### Equations

This theme supports rendering beautiful math in inline and display modes using [MathJax 3](https://www.mathjax.org/){:target="\_blank"} engine.
You just need to surround your math expression with `$$`, like `$$ E = mc^2 $$`.
If you leave it inside a paragraph, it will produce an inline expression, just like $$ E = mc^2 $$.

To use display mode, again surround your expression with `$$` and place it as a separate paragraph.
Here is an example:

$$
\left( \sum_{k=1}^n a_k b_k \right)^2 \leq \left( \sum_{k=1}^n a_k^2 \right) \left( \sum_{k=1}^n b_k^2 \right)
$$

### Citations

Citations are then used in the article body with the `<d-cite>` tag.
The key attribute is a reference to the id provided in the bibliography.
The key attribute can take multiple ids, separated by commas.

The citation is presented inline like this: <d-cite key="gregor2015draw"></d-cite> (a number that displays more information on hover).
If you have an appendix, a bibliography is automatically created and populated in it.

Distill chose a numerical inline citation style to improve readability of citation dense articles and because many of the benefits of longer citations are obviated by displaying more information on hover.
However, we consider it good style to mention author last names if you discuss something at length and it fits into the flow well — the authors are human and it’s nice for them to have the community associate them with their work.

### Footnotes

Just wrap the text you would like to show up in a footnote in a `<d-footnote>` tag.
The number of the footnote will be automatically generated.<d-footnote>This will become a hoverable footnote.</d-footnote>

### Code Blocks

Syntax highlighting is provided within `<d-code>` tags.
An example of inline code snippets: `<d-code language="html">let x = 10;</d-code>`.
For larger blocks of code, add a `block` attribute:

<d-code block language="javascript">
  var x = 25;
  function(x) {
    return x * x;
  }
</d-code>

### Images

Place images under `/assets/img/your_image.jpg`.

<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ site.baseurl }}/assets/img/7.jpg">
    </div>
</div>
<div class="caption">
    A simple, elegant caption looks good between image rows, after each row, or doesn't have to be there at all.
</div>
<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ site.baseurl }}/assets/img/8.jpg">
    </div>
    <div class="col-sm mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ site.baseurl }}/assets/img/10.jpg">
    </div>
</div>
