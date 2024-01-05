# 🌐Jinny's Blog

Built with Hexo and GitHub Pages. 

## Setup Hexo

[Hexo Documentation](https://hexo.io/docs/)

1. Install Node.js 
2. Install Hexo in terminal: `npm install -g hexo-cli`
3. Initializing a blog: `hexo init <folder name>`
4. Enter folder: `cd <folder name>`

## Customizing Blog

[Use Hexo Themes to customize the blog](https://hexo.io/themes/). The one I use is [Butterfly](https://butterfly.js.org/).

- In Hexo root file, install Butterfly theme: 

```shell
git clone -b master https://github.com/jerryc127/hexo-theme-butterfly.git themes/butterfly
```

- In `_config.yml`, change theme to butterfly.

- In Hexo root file, create a new theme config file `_config.butterfly.yml`.

- Install pug and stylus: 

```shell
npm install hexo-renderer-pug hexo-renderer-stylus --save
```

#### Change fonts in blog

- Fonts used: Noto Serif SC, Playfair Display

- In `_config.butterfly.yml`, change the global font settings:

```
font:
global-font-size: 17px
code-font-size: 16px
font-family: Ma Shan Zheng
code-font-family: consolas
```

- Embed the font as follow in `_config.butterfly.yml`:

```
inject:
head:
 <link rel="preconnect" href="https://fonts.googleapis.com">
 <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
 <link href="https://fonts.googleapis.com/css2?family=Noto+Serif+SC&display=swap" rel="stylesheet">
 <link href="https://fonts.googleapis.com/css2?family=Neuton&display=swap" rel="stylesheet">
```

#### Change colors in blog

- Color palette used: [Navy with white](https://colorhunt.co/palette/161a3031304db6bbc4f0ece5)

## Deploying

- Deploy and preview on local server.

```shell
npm install hexo-server --save
```

- Deploying to GitHub Pages

```shell
npm install hexo-deployer-git --save
```

- In ```_config.yml``` configure deploy settings: 

```
deploy:
type:git
repo: <repo link>
branch: gh-pages
```

- Hexo commands:

```
hexo clean
hexo generate
hexo deploy
```

- If there is any issues with deployment, please refer to the articles below:
  
  -  [针对github权限导致hexo部署失败的解决方案-CSDN博客](https://blog.csdn.net/weixin_30940783/article/details/99581061)
  
  - [解决 HTTP/2 stream 1 was not closed cleanly before end of the underlying stream-CSDN博客](https://blog.csdn.net/zz00008888/article/details/123529805)
  
  - [[解决 Failed to connect to github.com port 443:connection timed out-CSDN博客](https://blog.csdn.net/Hodors/article/details/103226958)](https://blog.csdn.net/zpf1813763637/article/details/128340109?utm_medium=distribute.pc_feed_404.none-task-blog-2~default~BlogCommendFromBaidu~activity-1-128340109-blog-null.262^v1^pc_404_mixedpudn&depth_1-utm_source=distribute.pc_feed_404.none-task-blog-2~default~BlogCommendFromBaidu~activity-1-128340109-blog-null.262^v1^pc_404_mixedpud)

```shell
git config --global http.version HTTP/1.1
git config --global --unset http.proxy
git config --global --unset https.proxy


```
