---
layout: post
title: "5分鐘建立GitHub Pages"
description: "從零開始建立GitHub Pages just like this!"
thumb_image: "documentation/sample-image.jpg"
tags: [web, jekyll]
---

{% include image.html path="documentation/chalk-intro.png" path-detail="documentation/chalk-intro@2x.png" alt="Chalk intro" %}

## 前言
身為一個資工系的學生，我想stackoverflow、medium或者痞客邦應該都不陌生對吧？多虧有這些平台以及大神們的文章，我才能平安的度過大學各種作業以及project（好人一生平安。而現在我站在巨人的肩膀上，來跟大家分享我是如何建立GitHub Pages like this !!

## WHY GitHub Pages
最主要的原因就是***簡單***!不用再去設定網域、帳號之類的，只需要開一個新的repository，再簡單的設定一下就好ㄌ，讚讚：）而且彈性比起medium、pixnet等來的大，可以根據你的需求再去微調。

## HOW GitHub Pages Like This 
本GitHub Pages使用[***Chalk***](https://github.com/nielsenramon/chalk)，來作為主題。接下來就會說明怎麼從零開始，搞出一個同樣的東西。

1.  Fork 到自己的帳號底下 
    {% include image.html path="github-pages/fork.png" path-detail="github-pages/fork.png" alt="Fork" %}
2. Change repository 名稱（Optional）
    {% include image.html path="github-pages/changeRepositoryName.png" path-detail="github-pages/changeRepositoryName.png" alt="Change Repository Name" %}
    - Repository 名稱為`github帳號.github.io`：網頁將會顯現在`github帳號.github.io`
    - Repository 名稱為`其他`：網頁將會顯現在`github帳號.github.io/其他` 

    所以要不要改名稱，It's up to you
3. 前置作業 <br>
    - macos : <br>
    `brew install ruby` <br>
    `brew install npm`
    - windows : <br>
        install [Ruby](https://rubyinstaller.org/) 
        [Node.js](https://nodejs.org/en/download/)

    這邊特別要注意的是ruby的版本，我自己的經驗是**2.7.3**可以，**3.0.0**則會出錯。
    都安裝好之後，打開terminal執行`npm run setup`，就會跑script去setup。
4. 在local端執行 <br>
{% include image.html path="github-pages/runLocal.png" path-detail="github-pages/runLocal.png" alt="Run Local" %}
    打開terminal輸入`npm run local`，如果都沒有問題的話，就能在`127.0.0.1:4000`看到你的網站了。你所有的改動只需一個重新整理，馬上就能看到。
5. Publish 到 GitHub Pages
    打開terminal輸入`npm run publish`，script會把你的改動push到gh-pages這個branch，稍等個幾分鐘就能看到改動了～

## 參考資料
- https://stackoverflow.com/questions/60198057/jekyll-wrong-number-of-arguments-given-2-expected-1-argumenterror
- https://stackoverflow.com/questions/65989040/bundle-exec-jekyll-serve-cannot-load-such-file