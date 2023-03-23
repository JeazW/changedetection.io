##网站变化监测、补货监控和通知

**_检测网站内容的变化并执行有意义的操作 - 通过 Discord、Email、Slack、Telegram、API 调用等方式触发通知以及更多其他方式._**

_积极地过好您的数据生活._ 


[<img src="https://raw.githubusercontent.com/dgtlmoon/changedetection.io/master/docs/screenshot.png" style="max-width:100%;" alt="Self-hosted web page change monitoring"  title="Self-hosted web page change monitoring"  />](https://lemonade.changedetection.io/start?src=github)

[![Release Version][release-shield]][release-link] [![Docker Pulls][docker-pulls]][docker-link] [![License][license-shield]](LICENSE.md)

![changedetection.io](https://github.com/dgtlmoon/changedetection.io/actions/workflows/test-only.yml/badge.svg?branch=master)

[**没有时间？让我们为您托管！尝试我们的每月 $8.99 的订阅服务 - 使用我们的代理并获得支持。!**](https://lemonade.changedetection.io/start) , _half the price of other website change monitoring services and comes with unlimited watches & checks!_

- 包括 Chrome 浏览器.
- 设置非常迅速，无需注册.
- 您可以立即开始观看网站变化通知。我们的服务速度非常快.


### 使用 Visual Selector 工具，我们可以选择网页的特定部分。这个工具非常直观和易于使用，您只需要用鼠标在网页上拖动，就可以选择您想监测的部分。l.

Available when connected to a <a href="https://github.com/dgtlmoon/changedetection.io/wiki/Playwright-content-fetcher">playwright content fetcher</a> (included as part of our subscription service)

[<img src="https://raw.githubusercontent.com/dgtlmoon/changedetection.io/master/docs/visualselector-anim.gif" style="max-width:100%;" alt="Self-hosted web page change monitoring context difference "  title="Self-hosted web page change monitoring context difference " />](https://lemonade.changedetection.io/start?src=github)

### 轻松查看变化内容，逐字、逐行或逐个字符检查.

[<img src="https://raw.githubusercontent.com/dgtlmoon/changedetection.io/master/docs/screenshot-diff.png" style="max-width:100%;" alt="Self-hosted web page change monitoring context difference "  title="Self-hosted web page change monitoring context difference " />](https://lemonade.changedetection.io/start?src=github)


### 执行交互式浏览器操作

使用填写文本框、点击按钮等方式，设置您的变化监测场景。

使用浏览器步骤配置，在执行变化监测之前添加基本步骤，比如登录网站、将商品添加到购物车、接受 cookie 登录、输入日期和优化搜索等。

<img src="docs/browsersteps-anim.gif" style="max-width:100%;" alt="Self-hosted web page change monitoring context difference "  title="Website change detection with interactive browser steps, login, cookies etc" />

在运行浏览器步骤之后，访问可视化选择器选项卡以优化您感兴趣的内容。
要求启用 Playwright。


### Example use cases

- 产品和服务的定价发生变化
- 了解缺货通知和重新上架通知
- 监测和跟踪 PDF 文件的变化，知道 PDF 文件是否有文字变化
- 政府部门更新（变化通常只在其网站上）
- 当您不在其邮件列表中时，监测新软件发布、安全警报等信息
- 节日变更
- Discogs 库存提醒和监测
- 房地产列表变化
- 在其他人之前得知您最喜欢的威士忌正在打折，或者其他特别优惠
- 从政府网站了解 COVID 相关新闻
- 从他们的网站获取大学/组织新闻
- 检测并监测 JSON API 响应的变化
- JSON API 监测和警报
- 法律文件和其他文件的变化
- 当网站上出现特定文本时通过通知触发 API 调用
- 通过 JSON 过滤器和 JSON 通知将 API 粘合在一起
- 基于 Web 内容的变化创建 RSS 订阅
- 监测 HTML 源代码的意外变化，加强您的 PCI 合规性
- 您有一个非常敏感的 URL 列表要监测，而且您不想使用付费的替代方案。（请记住，您 是产品）
- 在 Twitter 搜索结果中出现特定关键字时获得通知
- 主动寻找工作，当公司更新其招聘网页、搜索关键词时获得通知
- 在 Bamboo HR 和其他职位平台上发布新职位时获得通知
- 


_需要一个支持 Javascript 的 Chrome 运行器吗？我们支持通过 WebDriver 和 Playwright 进行获取！</a>_

#### Key Features

- 提供许多触发器过滤器，例如“基于文本触发”、“通过选择器删除文本”、“忽略文本”、“提取文本”，还可使用正则表达式！
- 使用 xPath 和 CSS 选择器来定位元素，使用 JSONPath 或 jq 轻松监视复杂的 JSON。
- 切换快速的非 JS 和基于 Chrome JS 的“提取器”。
- 跟踪 PDF 文件的更改（监视 PDF 中的文本更改，同时监视 PDF 的文件大小和校验和）。
- 轻松指定网站应该检查的频率。
- 在提取文本之前执行 JS（适用于登录，可在 UI 中查看示例！）。
- 覆盖请求头，指定“POST”或“GET”等方法。
- 使用“可视化选择器”来帮助定位特定元素。
- 可配置的每个监视的代理。
- 当检测到网页更改时，发送包含截图的通知。

We [recommend and use Bright Data](https://brightdata.grsm.io/n0r16zf7eivq) global proxy services, Bright Data will match any first deposit up to $100 using our signup link.

Please :star: star :star: this project and help it grow! https://github.com/dgtlmoon/changedetection.io/

## Installation

### Docker

With Docker composer, just clone this repository and..

```bash
$ docker-compose up -d
```

Docker standalone
```bash
$ docker run -d --restart always -p "127.0.0.1:5000:5000" -v datastore-volume:/datastore --name changedetection.io dgtlmoon/changedetection.io
```

`:latest` tag is our latest stable release, `:dev` tag is our bleeding edge `master` branch.

Alternative docker repository over at ghcr - [ghcr.io/dgtlmoon/changedetection.io](https://ghcr.io/dgtlmoon/changedetection.io)

### Windows

See the install instructions at the wiki https://github.com/dgtlmoon/changedetection.io/wiki/Microsoft-Windows

### Python Pip

Check out our pypi page https://pypi.org/project/changedetection.io/

```bash
$ pip3 install changedetection.io
$ changedetection.io -d /path/to/empty/data/dir -p 5000
```

Then visit http://127.0.0.1:5000 , You should now be able to access the UI.

_Now with per-site configurable support for using a fast built in HTTP fetcher or use a Chrome based fetcher for monitoring of JavaScript websites!_

## Updating changedetection.io

### Docker
```
docker pull dgtlmoon/changedetection.io
docker kill $(docker ps -a -f name=changedetection.io -q)
docker rm $(docker ps -a -f name=changedetection.io -q)
docker run -d --restart always -p "127.0.0.1:5000:5000" -v datastore-volume:/datastore --name changedetection.io dgtlmoon/changedetection.io
```

### docker-compose

```bash
docker-compose pull && docker-compose up -d
```

See the wiki for more information https://github.com/dgtlmoon/changedetection.io/wiki


## Filters

XPath、JSONPath、jq和CSS支持已经内置！你可以根据需要进行精确定位，可以使用从各种XPath元素查询创建工具中导出的XPath。
(We support LXML `re:test`, `re:math` and `re:replace`.)

## Notifications

ChangeDetection.io supports a massive amount of notifications (including email, office365, custom APIs, etc) when a web-page has a change detected thanks to the <a href="https://github.com/caronc/apprise">apprise</a> library.
Simply set one or more notification URL's in the _[edit]_ tab of that watch.

Just some examples

    discord://webhook_id/webhook_token
    flock://app_token/g:channel_id
    gitter://token/room
    gchat://workspace/key/token
    msteams://TokenA/TokenB/TokenC/
    o365://TenantID:AccountEmail/ClientID/ClientSecret/TargetEmail
    rocket://user:password@hostname/#Channel
    mailto://user:pass@example.com?to=receivingAddress@example.com
    json://someserver.com/custom-api
    syslog://
 
<a href="https://github.com/caronc/apprise#popular-notification-services">And everything else in this list!</a>

<img src="https://raw.githubusercontent.com/dgtlmoon/changedetection.io/master/docs/screenshot-notifications.png" style="max-width:100%;" alt="Self-hosted web page change monitoring notifications"  title="Self-hosted web page change monitoring notifications"  />

Now you can also customise your notification content and use <a target="_new" href="https://jinja.palletsprojects.com/en/3.0.x/templates/">Jinja2 templating</a> for their title and body!

## JSON API Monitoring

Detect changes and monitor data in JSON API's by using either JSONPath or jq to filter, parse, and restructure JSON as needed.

![image](https://raw.githubusercontent.com/dgtlmoon/changedetection.io/master/docs/json-filter-field-example.png)

This will re-parse the JSON and apply formatting to the text, making it super easy to monitor and detect changes in JSON API results

![image](https://raw.githubusercontent.com/dgtlmoon/changedetection.io/master/docs/json-diff-example.png)

### JSONPath or jq?

For more complex parsing, filtering, and modifying of JSON data, jq is recommended due to the built-in operators and functions. Refer to the [documentation](https://stedolan.github.io/jq/manual/) for more specifc information on jq.

One big advantage of `jq` is that you can use logic in your JSON filter, such as filters to only show items that have a value greater than/less than etc.

See the wiki https://github.com/dgtlmoon/changedetection.io/wiki/JSON-Selector-Filter-help for more information and examples

### Parse JSON embedded in HTML!

When you enable a `json:` or `jq:` filter, you can even automatically extract and parse embedded JSON inside a HTML page! Amazingly handy for sites that build content based on JSON, such as many e-commerce websites. 

```
<html>
...
<script type="application/ld+json">

{
   "@context":"http://schema.org/",
   "@type":"Product",
   "offers":{
      "@type":"Offer",
      "availability":"http://schema.org/InStock",
      "price":"3949.99",
      "priceCurrency":"USD",
      "url":"https://www.newegg.com/p/3D5-000D-001T1"
   },
   "description":"Cobratype King Cobra Hero Desktop Gaming PC",
   "name":"Cobratype King Cobra Hero Desktop Gaming PC",
   "sku":"3D5-000D-001T1",
   "itemCondition":"NewCondition"
}
</script>
```  

`json:$..price` or `jq:..price` would give `3949.99`, or you can extract the whole structure (use a JSONpath test website to validate with)

The application also supports notifying you that it can follow this information automatically


## Proxy Configuration

See the wiki https://github.com/dgtlmoon/changedetection.io/wiki/Proxy-configuration , we also support using [BrightData proxy services where possible]( https://github.com/dgtlmoon/changedetection.io/wiki/Proxy-configuration#brightdata-proxy-support)

## Raspberry Pi support?

Raspberry Pi and linux/arm/v6 linux/arm/v7 arm64 devices are supported! See the wiki for [details](https://github.com/dgtlmoon/changedetection.io/wiki/Fetching-pages-with-WebDriver)

## API Support

Supports managing the website watch list [via our API](https://changedetection.io/docs/api_v1/index.html)

## Support us

Do you use changedetection.io to make money? does it save you time or money? Does it make your life easier? less stressful? Remember, we write this software when we should be doing actual paid work, we have to buy food and pay rent just like you.


Firstly, consider taking out a [change detection monthly subscription - unlimited checks and watches](https://lemonade.changedetection.io/start) , even if you don't use it, you still get the warm fuzzy feeling of helping out the project. (And who knows, you might just use it!)

Or directly donate an amount PayPal [![Donate](https://img.shields.io/badge/Donate-PayPal-green.svg)](https://www.paypal.com/donate/?hosted_button_id=7CP6HR9ZCNDYJ)

Or BTC `1PLFN327GyUarpJd7nVe7Reqg9qHx5frNn`

<img src="https://raw.githubusercontent.com/dgtlmoon/changedetection.io/master/docs/btc-support.png" style="max-width:50%;" alt="Support us!"  />

## Commercial Support

I offer commercial support, this software is depended on by network security, aerospace , data-science and data-journalist professionals just to name a few, please reach out at dgtlmoon@gmail.com for any enquiries, I am more than glad to work with your organisation to further the possibilities of what can be done with changedetection.io


[release-shield]: https://img.shields.io:/github/v/release/dgtlmoon/changedetection.io?style=for-the-badge
[docker-pulls]: https://img.shields.io/docker/pulls/dgtlmoon/changedetection.io?style=for-the-badge
[test-shield]: https://github.com/dgtlmoon/changedetection.io/actions/workflows/test-only.yml/badge.svg?branch=master

[license-shield]: https://img.shields.io/github/license/dgtlmoon/changedetection.io.svg?style=for-the-badge
[release-link]: https://github.com/dgtlmoon/changedetection.io/releases
[docker-link]: https://hub.docker.com/r/dgtlmoon/changedetection.io
