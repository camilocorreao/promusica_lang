---
title: "2023 09 03  Test Post"
date: 2023-09-03T16:29:51+02:00
draft: false
categories: ["planet express"]
tags: [human]
images: [AmyWong.png]
---

Lorem ipsum dolor sit amet consectetur adipisicing elit. Quidem voluptatibus aperiam ab distinctio? Quia aliquam, laudantium numquam saepe sit, ipsa aliquid magni doloremque fugit asperiores ullam illo, esse eius necessitatibus quaerat sint. Tempore, veniam distinctio. Natus libero accusantium quos vel.

{{< img-index "0" "Test Post Picture" >}}

```go-html-template
{{/*  production options  */}}
{{- $opts := dict "minify" true "target" "es2015" -}}
{{- /*  development options  */ -}}
{{- if eq hugo.Environment "development" -}}
{{- $opts = dict "sourceMap" "inline" "target" "es2015" -}}
{{- end -}}
{{- $built := resources.Get . | js.Build $opts | fingerprint }}

<script type="text/javascript" src="{{ $built.RelPermalink }}" integrity="{{ $built.Data.Integrity }}"></script>
```
