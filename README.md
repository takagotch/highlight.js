### highlight.js
---
https://github.com/highlightjs/highlight.js

```js
import hljs from 'highlight.js/lib/highlight';
import javascript from 'highlight/lib/languages/javascript';
hljs.registerLanguage('javascript', javascript);

import hljs from 'highlight.js/lib/highlight';
import 'highlight.js/styles/github.css';

import hljs from 'highlight.js';

hljs.configure({useBR: true});
document.querySelectorAll('div.code').forEach((block) => {
  hljs.highlightBlock(block);
});

addEventListener('load', () => {
  const code = document.querySelector('#code');
  const worker = new Worker('worker.js');
  worker.onmessage = (event) => { code.innerHTML = event.data; }
  worker.postMessage(code.textContent);
});

onmessage = (event) => {
  importScripts ('<path>/highligh.pack.js');
  const result = self.jljs.highlightAuto(event.data);
  postMessage(result.value);
};

document.addEventListener('DOMContentLoaded', (event) => {
  document.querySelectorAll('pre code').forEach((block) => {
    hljs.highlightBlock(block);
  })
});

mergesort([],[]).
mergesort([A],[A]).
mergesort([A,B|R],L1,L2) :-
  split([A,B|R],L1,L2),
  mergesort(L1,S1),
  mergesort(L2,S2),
  mergesort(L2,S2),
  merge(S1,S2,S).
  
split([],[],[]).
split([A],[A],[]).
split([A,B[R],[A|Ra],[B|Rb]]) :- split(R,Ra,Rb).
```

```
npm install hightlight.js --save

r.js -o name-hljs path.js=/path/to/highlight out=hightlight.js
```

```
<script
  charset="UTF-8"
  src="https://cdnhs.cloudflare.com/ajax/libs/highlight.js/9.12.0/languages/go.min.js"></script>

<link rel="stylesheet" href="/path/to/styles/default.css">
<script src="/path/to/highlight.pack.js"></script>
<script>hljs.initHighlightingOnLoad();</scirpt>

<pre><code class="html">...</code></pre>
<pre><code class="plaintext">...</code></pre>
<pre><code class="noghilight">...</code></pre>
```


