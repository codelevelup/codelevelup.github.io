---
title: "Layout: Header Video"
author: marche798
excerpt: "show excert Layout: Header Video"
# excerpt_separator: "<!--more-->"
header:
  teaser: "assets/images/500x300.png"
categories:
  - Java
  - Spring
tags:
  - video
  - layout
toc: true
last_modified_at: 2018-01-07T12:29:16-04:00
---

This post should display a **header with a responsive video**, if the theme supports it.

## Settings

| Parameter  | Required     | Description |
|----------  |---------     | ----------- |
| `id`       | **Required** | ID of the video |
| `provider` | **Required** | Hosting provider of the video, either `youtube` or `vimeo` |

### YouTube

To embed the following YouTube video at url `https://www.youtube.com/watch?v=XsxDH4HcOWA` (long version) or `https://youtu.be/XsxDH4HcOWA` (short version) into a post or page's main content you'd use:

```liquid
{% raw %}{% include video id="XsxDH4HcOWA" provider="youtube" %}{% endraw %}
```

{% include video id="XsxDH4HcOWA" provider="youtube" %}

To embed it as a video header you'd use the following YAML Front Matter

```yaml
header:
  video:
    id: XsxDH4HcOWA
    provider: youtube
```

### Vimeo

To embed the following Vimeo video at url `https://vimeo.com/97649261` into a post or page's main content you'd use:

```liquid
{% raw %}{% include video id="97649261" provider="vimeo" %}{% endraw %}
```

{% include video id="97649261" provider="vimeo" %}

To embed it as a video header you'd use the following YAML Front Matter

```yaml
header:
  video:
    id: 97649261
    provider: vimeo
```
