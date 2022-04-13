jquery-resizable-columns
=======================

Resizable table columns for jQuery. **[Live Demo](http://dobtco.github.io/jquery-resizable-columns)**

**New and Improved!** *Now tested and working on Chrome & Firefox (Mac + Windows), and IE 9 + 10. Other browsers might work too, just haven't had time to check.*

**Size:** < 8kb minified

---

I made some changes to the original author's above

if you used `bootstrap-table` ,you can also see [https://github.com/thetbw/bootstrap-table](https://github.com/thetbw/bootstrap-table/commit/e3f39b648f52c0f8703d67e2047f9f4999648f83)

It's not perfect, and some you may need to modify yourself

if you want build by you self,maybe you need create a file named `npm-shrinkwrap.json` in
project root,and add this content,because origin dependencies was so old.
```json
{
"dependencies": {
  "graceful-fs": {
      "version": "4.2.2"
    }
  }
}
```

**bugfix change log:**
* Change table layout to 'fixed'
* Change from percentage width to pixel width

#### Dependencies
- jQuery
- [store.js](https://github.com/marcuswestin/store.js/) (or anything similar) for localStorage persistence.

#### Simple Usage

```
<table>
  <thead>
    <tr>
      <th>#</th>
      <th>First Name</th>
      <th>Last Name</th>
      <th>Username</th>
    </tr>
  </thead>
  <tbody>
    ...
  </tbody>
</table>

<script>
  $(function(){
    $("table").resizableColumns();
  });
</script>
```

#### Persist column sizes

To save column sizes on page reload (or js re-rendering), just pass an object that responds to `get` and `set`. You'll also have to give your &lt;table&gt; a `data-resizable-columns-id` attribute, and your &lt;th&gt;s `data-resizable-column-id` attributes.

```
<script src="libs/jquery.js"></script>
<script src="libs/store.js"></script>
<script src="jquery.resizableColumns.js"></script>

<table data-resizable-columns-id="demo-table">
  <thead>
    <tr>
      <th data-resizable-column-id="#">#</th>
      <th data-resizable-column-id="first_name">First Name</th>
      <th data-resizable-column-id="last_name">Last Name</th>
      <th data-resizable-column-id="username">Username</th>
    </tr>
  </thead>
  <tbody>
    ...
  </tbody>
</table>

<script>
  $(function(){
    $("table").resizableColumns({
      store: store
    });
  });
</script>
```

#### License

MIT

#### Credits

There's various versions of this plugin floating around the internet, but they're all outdated in one way or another. Thanks to [http://robau.wordpress.com/2011/06/09/unobtrusive-table-column-resize-with-jquery/]() for a great starting point.
