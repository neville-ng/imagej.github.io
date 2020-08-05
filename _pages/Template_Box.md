<includeonly><div
{{#if:{{{id|}}}|id="{{{id|}}}"}}
        style="{{#ifeq: {{{float|}}} | left | float:left; | {{#ifeq: {{{float|}}} | right | float:right; | margin: 0 auto;}}}}
        width: {{#if:{{{width|}}}|{{{width|}}}|300px}};
        border: 1px solid #ccc;
        padding: 15px !important;
        margin-top: 1em;
        margin-bottom: 2em;
        background-color: {{#if:{{{bgcolor|}}}|{{{bgcolor}}}|#ffefbe}};
        {{border-radius|.75em}}{{box-shadow}}">
{{#if:{{{title|}}}|<p style="font-size: large; font-weight: bold; margin-top: 0; padding-top: 0">{{{title}}}</p>}} {{{text|{{{1}}}|}}}</div></includeonly>
<noinclude>
==Usage==
<pre>
{{Box | The quick brown fox jumped over the lazy dog.}}
</pre>
{{Box | The quick brown fox jumped over the lazy dog.}}
<pre>
{{Box | float=left | How much wood could a woodchuck chuck if a woodchuck could chuck wood?}}
</pre>
{{Box | float=left | How much wood could a woodchuck chuck if a woodchuck could chuck wood?}}
<div style="clear: left;"></div>
<pre>
{{Box
| title = Announcing new Shimmer!
| text = New Shimmer is both a floor wax and a dessert topping! Here, I'll spray some on your mop.
| width = 40%
| float = right
}}
</pre>
{{Box
| title = Announcing new Shimmer!
| text = New Shimmer is both a floor wax and a dessert topping! Here, I'll spray some on your mop.
| width = 40%
| float = right
}}
<div style="clear: right;"></div>
<pre>
{{Box
| title = Do you like green eggs and ham?
| text = I like green eggs and ham!<br>I do! I like them, Sam-I-am!
| bgcolor = palegreen
}}
</pre>
{{Box
| title = Do you like green eggs and ham?
| text = I like green eggs and ham!<br>I do! I like them, Sam-I-am!
| bgcolor = palegreen
}}

[[Category:Boxes]]
</noinclude>