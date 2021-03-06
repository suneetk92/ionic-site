---
layout: "v2_fluid/docs_base"
version: "2.0.0-beta.1"
versionHref: "/docs/v2/2.0.0-beta.1"
path: ""
category: api
id: "content"
title: "Content"
header_sub_title: "Class in module "
doc: "Content"
docType: "class"

---









<h1 class="api-title">


Content






</h1>

<a class="improve-v2-docs" href='http://github.com/driftyco/ionic/edit/2.0/ionic/components/content/content.ts#L8'>
Improve this doc
</a>






<p>The Content component provides an easy to use content area that can be configured to use Ionic&#39;s custom Scroll View, or the built in overflow scrolling of the browser.</p>
<p>While we recommend using the custom Scroll features in Ionic in most cases, sometimes (for performance reasons) only the browser&#39;s native overflow scrolling will suffice, and so we&#39;ve made it easy to toggle between the Ionic scroll implementation and overflow scrolling.</p>
<p>You can implement pull-to-refresh with the <a href="../../scroll/Refresher">Refresher</a> component.</p>


<h2>Component</h2>
<h3>selector: <code>ion-content</code></h3>
<!-- @usage tag -->

<h2>Usage</h2>

<pre><code class="lang-html">&lt;ion-content id=&quot;myContent&quot;&gt;
  Add your content here!
&lt;/ion-content&gt;
</code></pre>




<!-- @property tags -->



<!-- instance methods on the class -->

<h2>Instance Methods</h2>

<div id="onScrollEnd"></div>

<h3>
<code>onScrollEnd(callback)</code>
  

</h3>

Call a method when scrolling has stopped



<table class="table param-table" style="margin:0;">
  <thead>
    <tr>
      <th>Param</th>
      <th>Type</th>
      <th>Details</th>
    </tr>
  </thead>
  <tbody>
    
    <tr>
      <td>
        callback
        
        
      </td>
      <td>
        
  <code>Function</code>
      </td>
      <td>
        <p>The method you want perform when scrolling has ended</p>

        
      </td>
    </tr>
    
  </tbody>
</table>








<div id="scrollTo"></div>

<h3>
<code>scrollTo(x,&nbsp;y,&nbsp;duration,&nbsp;tolerance)</code>
  

</h3>

Scroll to the specified position.

```ts
@Page({
  template: `<ion-content id="my-content">
     <button (click)="scrollTo()"> Down 500px</button>
  </ion-content>`
)}
export class MyPage{
   constructor(app: IonicApp){
       this.app = app;
   }
  // Need to wait until the component has been initialized
  ngAfterViewInit() {
    // Here 'my-content' is the ID of my ion-content
    this.content = this.app.getComponent('my-content');
  }
   scrollTo() {
     this.content.scrollTo(0, 500, 200);
   }
}
```


<table class="table param-table" style="margin:0;">
  <thead>
    <tr>
      <th>Param</th>
      <th>Type</th>
      <th>Details</th>
    </tr>
  </thead>
  <tbody>
    
    <tr>
      <td>
        x
        
        
      </td>
      <td>
        
  <code>number</code>
      </td>
      <td>
        <p>The x-value to scroll to.</p>

        
      </td>
    </tr>
    
    <tr>
      <td>
        y
        
        
      </td>
      <td>
        
  <code>number</code>
      </td>
      <td>
        <p>The y-value to scroll to.</p>

        
      </td>
    </tr>
    
    <tr>
      <td>
        duration
        
        
      </td>
      <td>
        
  <code>number</code>
      </td>
      <td>
        <p>Duration of the scroll animation in ms.</p>

        
      </td>
    </tr>
    
    <tr>
      <td>
        tolerance
        
        
      </td>
      <td>
        
  <code>TODO</code>
      </td>
      <td>
        <p>TODO</p>

        
      </td>
    </tr>
    
  </tbody>
</table>





<div class="return-value">
<i class="icon ion-arrow-return-left"></i>
<b>Returns:</b> 
  <code>Promise</code> Returns a promise when done
</div>




<div id="scrollToTop"></div>

<h3>
<code>scrollToTop()</code>
  

</h3>

Scroll to the specified position.

```ts
@Page({
  template: `<ion-content id="my-content">
     <button (click)="scrollTop()"> Down 500px</button>
  </ion-content>`
)}
export class MyPage{
   constructor(app: IonicApp){
       this.app = app;
   }
  // Need to wait until the component has been initialized
  ngAfterViewInit() {
    // Here 'my-content' is the ID of my ion-content
    this.content = this.app.getComponent('my-content');
  }
   scrollTop() {
     this.content.scrollTop();
   }
}
```






<div class="return-value">
<i class="icon ion-arrow-return-left"></i>
<b>Returns:</b> 
  <code>Promise</code> Returns a promise when done
</div>


<!-- related link --><!-- end content block -->


<!-- end body block -->

