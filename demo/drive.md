---
layout: default
title: Tiny Drive
title_nav: Tiny Drive
description_short: Tiny Drive
description: Tiny Drive. A premium plugin to manage files & images.
keywords: tinydrive .net php relative_urls
---

## Live example

This example shows you how to use Tiny Drive for your file and image management. For more information on the Tiny Drive plugin, see the [docs]({{site.baseurl}}/plugins/drive/).

<textarea>
<h2>The world's first rich text editor in the cloud</h2>
<p>Have you heard about Tiny Cloud? It's the first step in our journey to help you deliver great content creation experiences, no matter your level of expertise. 50,000 developers already agree. They get free access to our global Content Delivery Network, image proxy services and auto updates to the TinyMCE editor. They're also ready for some exciting updates coming soon.</p>
<p>One of these enhancements is <strong>Tiny Drive</strong>: imagine file management for TinyMCE, in the cloud, made super easy. Learn more at <a href="tinydrive/">our working demo</a>, where you'll find an opportunity to provide feedback to the product team.</p>
<h3>An editor for every project</h3>
<p>Here are some of our customer's most common use cases for TinyMCE:</p>
<ul>
<li>Content Management Systems (<em>WordPress, Umbraco</em>)</li>
<li>Learning Management Systems (<em>Blackboard</em>)</li>
<li>Customer Relationship Management and marketing automation (<em>Marketo</em>)</li>
<li>Email marketing (<em>Constant Contact</em>)</li>
<li>Content creation in SaaS systems (<em>Eventbrite, Evernote, GoFundMe, Zendesk</em>)</li>
</ul>
<p>&nbsp;</p>
<p>And those use cases are just the start. TinyMCE is incredibly flexible, and with hundreds of APIs there's likely a solution for your editor project. If you haven't experienced Tiny Cloud, get started today. You'll even get a free premium plugin trial &ndash; no credit card required!</p>
</textarea>
<style>
  button.olark-launch-button {
    z-index: 1 !important;
  }
  .menu {
    z-index: 1000 !important;
  }
</style>

<script src="https://devpreview.tiny.cloud/demo/tinymce.min.js"></script>
<script>

tinymce.init({
  selector: 'textarea',
  plugins: 'image media link tinydrive code imagetools',
  api_key: 'fake-key',
  content_css: [
    "//fonts.googleapis.com/css?family=Lato|Lobster|Noto+Serif|Permanent+Marker|Raleway|Roboto|Source+Code+Pro",
    "//tiny.cloud/css/content-standard.min.css"
  ],
  height: 600,
  imagetools_cors_hosts: ['picsum.photos'],
  tinydrive_token_provider: (success, failure) => {
    success({ token: 'eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJzdWIiOiJqb2huZG9lIiwibmFtZSI6IkpvaG4gRG9lIiwiaWF0IjoxNTE2MjM5MDIyfQ.Ks_BdfH4CWilyzLNk8S2gDARFhuxIauLa8PwhdEQhEo' });
  },
  tinydrive_demo_files_url: '{{ site.baseurl }}/demo/tiny-drive-demo/demo_files.json',
  toolbar: 'insertfile image link | code'
});

</script>

### Code:

```js
tinymce.init({
  selector: 'textarea',
  plugins: 'image media link tinydrive code imagetools',
  api_key: 'YOUR_API_KEY',
  height: 600,
  tinydrive_token_provider: 'URL_TO_YOUR_TOKEN_PROVIDER',
  toolbar: 'insertfile image link | code'
});
```