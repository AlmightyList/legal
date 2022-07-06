# legal

This is a repo for PUBLIC legal docs. DON'T put sensitive info in here.

The docs folder is served as a static site via the github pages system. This allows us to access content files (with a single source of truth) from multiple places.

### Buyer code snippet for wix

```
<div id="render-terms-of-trade"></div>
<script src="https://cdnjs.cloudflare.com/ajax/libs/markdown-it/13.0.1/markdown-it.min.js"></script>
<script>
  var styleEl = document.createElement('style')
  styleEl.type = 'text/css';
  styleEl.appendChild(document.createTextNode(`
    @import url('https://fonts.googleapis.com/css2?family=Roboto:wght@400;700&display=swap');
    #render-terms-of-trade {
      line-height: 1.5rem;
      font-family: 'Roboto', sans-serif;}
    #render-terms-of-trade ul {
      list-style-type: none;}
    #render-terms-of-trade ul li {
      margin-bottom: 1rem;}
    #render-terms-of-trade ul li ul li {
      margin-bottom: 0rem;}
  `))
  document.head.append(styleEl)
  var termsOfTrade = 'https://almightylist.github.io/legal/terms-of-trade-buyer.md'
  var md = new markdownit()
  var renderLocation = document.getElementById('render-terms-of-trade');
  fetch(termsOfTrade)
    .then((response) => {
      return response.text();
    })
    .then((data) => {
      renderLocation.innerHTML = md.render(data)
    });
</script>
```

### Supplier code snippet for wix

```
<div id="render-terms-of-trade"></div>
<script src="https://cdnjs.cloudflare.com/ajax/libs/markdown-it/13.0.1/markdown-it.min.js"></script>
<script>
  var styleEl = document.createElement('style')
  styleEl.type = 'text/css';
  styleEl.appendChild(document.createTextNode(`
    @import url('https://fonts.googleapis.com/css2?family=Roboto:wght@400;700&display=swap');
    #render-terms-of-trade {
      line-height: 1.5rem;
      font-family: 'Roboto', sans-serif;}
    #render-terms-of-trade ul {
      list-style-type: none;}
    #render-terms-of-trade ul li {
      margin-bottom: 1rem;}
    #render-terms-of-trade ul li ul li {
      margin-bottom: 0rem;}
  `))
  document.head.append(styleEl)
  var termsOfTrade = 'https://almightylist.github.io/legal/terms-of-trade-supplier.md'
  var md = new markdownit()
  var renderLocation = document.getElementById('render-terms-of-trade');
  fetch(termsOfTrade)
    .then((response) => {
      return response.text();
    })
    .then((data) => {
      renderLocation.innerHTML = md.render(data)
    });
</script>
```
