# Router-Link中的router-Link-Exact-Active问题

## 什么是router-link-exact-active？
router-link-exact-active 是 Vue Router 中的一个属性，用于在页面导航时与路由页面绑定以实现精确的活动链接高亮效果。它是 &lt;router-link&gt; 组件的一个属性，用于检测当前路由是否与链接的 to 属性完全匹配。

当实现页面导航时与路由页面绑定效果时，有两种方法：

1.在router-link标签中绑定类，通过在style中设置类的样式完成link的高亮或其他效果，示例代码如下：

`&lt;template&gt;
  &lt;div&gt;
    &lt;router-link to=&#34;/&#34; exact-active-class=&#34;active&#34;&gt;Home&lt;/router-link&gt;
    &lt;router-link to=&#34;/about&#34; exact-active-class=&#34;active&#34;&gt;About&lt;/router-link&gt;
    &lt;router-link to=&#34;/contact&#34; exact-active-class=&#34;active&#34;&gt;Contact&lt;/router-link&gt;
  &lt;/div&gt;
&lt;/template&gt;`

`.active {
font-weight: bold;
color: blue;
}`

2.直接在style中调用link的属性，从而设置其高亮或其他效果，完成绑定。代码如下：



## 两种绑定效果有什么区别呢？
在 Vue.js 中，将 `.router-link-exact-active `样式规则设置在样式表（style）中和将其直接设置在 &lt;router-link&gt; 组件标签上的效果是不同的。

设置在样式表中：如果你将 `.router-link-exact-active `样式规则设置在样式表中（如你之前提供的样式代码），那么这个样式规则将会应用到所有使用 Vue Router 的链接，不需要在每个链接上重复设置。这是一种更为统一和集中管理样式的方式。任何精确匹配的链接都会自动具有指定的样式。

在 `&lt;router-link&gt; `组件上设置：如果你在单个 `&lt;router-link&gt; `组件上设置 class 属性来指定 `.router-link-exact-active `样式类，那么这个样式类仅会应用到该具体链接。这是一种更为特定和个性化的方式，允许你为不同的链接指定不同的样式类，从而实现不同的高亮效果。

通常，如果你希望所有精确匹配的链接都具有相同的高亮效果，最好将` .router-link-exact-active `样式规则设置在样式表中。如果你需要不同的链接有不同的高亮效果，可以在链接上设置 class 属性以覆盖全局样式。

选择哪种方式取决于你的设计需求和样式管理的偏好。

---

> 作者: Toserhy  
> URL: http://localhost:1313/posts/active/  

