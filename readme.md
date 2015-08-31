개발 및 정책 문서
=======

Toss Pay 는 ...

![](http://2.bp.blogspot.com/-FsmE4jGmZHk/U8kXcyRUBwI/AAAAAAAAKb4/g2n6v-sq_Tc/s1600/hula-minion.png)

개발 가이드
---------------

### 시작하기

To fetch a Github Repository's readme file, use the `Flatdoc.github` fetcher.
This will fetch the Readme file of the repository's default branch.

``` javascript
Flatdoc.run({
  fetcher: Flatdoc.github('USER/REPO')
});
```

You may also fetch another file other than the Readme file, just specify it as
the 2nd parameter.

``` javascript
Flatdoc.run({
  fetcher: Flatdoc.github('USER/REPO', 'Changelog.md')
});
```

After you've done this, you probably want to deploy it via [GitHub Pages].

[GitHub Pages guide >][GitHub Pages]

### Toss 결제 개요

You may also fetch a file. In this example, this fetches the file `Readme.md` in
the same folder as the HTML file.

``` javascript
Flatdoc.run({
  fetcher: Flatdoc.file('Readme.md')
});
```

You may actually supply any URL here. It will be fetched via AJAX. This is
useful for local testing.

``` javascript
Flatdoc.run({
  fetcher: Flatdoc.file('http://yoursite.com/Readme.md')
});
```

정책
------------

Flatdoc is a hosted `.js` file (along with a theme and its assets) that you can
add into any page hosted anywhere.

#### 결제 생성

There are no build scripts or 3rd-party services involved. Everything is done in
the browser. Worried about performance? Oh, It's pretty fast.

Flatdoc utilizes the [GitHub API] to fetch your project's Readme files. You may
also configure it to fetch any arbitrary URL via AJAX.

#### 결제 취소 및 환불

Next, it uses [marked], an extremely fast Markdown parser that has support for
GitHub flavored Markdown.

Flatdoc then simply renders *menu* and *content* DOM elements to your HTML
document. Flatdoc also comes with a default theme to style your page for you, or
you may opt to create your own styles.

