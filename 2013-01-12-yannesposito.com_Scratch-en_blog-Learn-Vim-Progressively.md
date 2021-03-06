<div id="content">
            <div id="choix">
                <div class="return"><a href="#entete">↓ Menu ↓</a></div>
                <div id="choixlang"><a href="/Scratch/fr/blog/Learn-Vim-Progressively/" onclick="setLanguage('fr')">en Français</a>
                </div>
  			<script type="text/javascript">// <![CDATA[
				document.write('<div id="switchcss"><a href="#">Switch style</a></div>');
				// ]]>
				</script><div id="switchcss"><a href="#">Switch style</a></div>
                <div class="flush"></div>
            </div>
            <div id="titre">
                <h1>
                    Learn Vim Progressively
                </h1>
                
            </div>
            <div class="flush"></div>

            

            

            <div class="flush"></div>
            <div id="afterheader">
                <div class="corps">
                    <img alt="Über leet use vim!" src="/Scratch/img/blog/Learn-Vim-Progressively/uber_leet_use_vim.jpg">


<div class="intro">


<p><span class="sc"><abbr title="Too long; didn't read">tl;dr</abbr>: </span> You want to teach yourself vim (the best text editor known to human kind) in the fastest way possible. This my way of doing it. You start by learning the minimal to survive, then you integrate all the tricks slowly.</p>


</div>


<p><a href="http://www.vim.org">Vim</a> the Six Billion Dollar editor</p>

<blockquote>
  <p>Better, Stronger, Faster.</p>
</blockquote>

<p>Learn <a href="http://www.vim.org">vim</a> and it will be your last text editor.
There isn’t any better text editor that I know of.
It is hard to learn, but incredible to use.</p>

<p>I suggest you teach yourself Vim in 4 steps:</p>

<ol>
  <li>Survive</li>
  <li>Feel comfortable</li>
  <li>Feel Better, Stronger, Faster</li>
  <li>Use superpowers of vim</li>
</ol>

<p>By the end of this journey, you’ll become a vim superstar. </p>

<p>But before we start, just a warning.
Learning vim will be painful at first.
It will take time.
It will be a lot like playing a musical instrument.
Don’t expect to be more efficient with vim than with another editor in less than 3 days.
In fact it will certainly take 2 weeks instead of 3 days.</p>

<h2 id="st-level----survive">1<sup>st</sup> Level – Survive</h2>

<ol>
  <li>Install <a href="http://www.vim.org">vim</a></li>
  <li>Launch vim</li>
  <li>DO NOTHING! Read.</li>
</ol>

<p>In a standard editor, typing on the keyboard is enough to write something and see it on the screen.
Not this time.
Vim is in <em>Normal</em> mode.
Let’s go to <em>Insert</em> mode.
Type the letter <code>i</code>.</p>

<p>You should feel a bit better.
You can type letters like in a standard editor.
To get back to <em>Normal</em> mode just press the <code>ESC</code> key.</p>

<p>You now know how to switch between <em>Insert</em> and <em>Normal</em> mode.
And now, here are the commands that you need in order to survive in <em>Normal</em> mode:</p>

<blockquote>
  <ul>
    <li><code>i</code> → <em>Insert</em> mode. Type <code>ESC</code> to return to Normal mode.</li>
    <li><code>x</code> → Delete the char under the cursor</li>
    <li><code>:wq</code> → Save and Quit (<code>:w</code> save, <code>:q</code> quit)</li>
    <li><code>dd</code> → Delete (and copy) the current line</li>
    <li><code>p</code> → Paste</li>
  </ul>

  <p>Recommended:</p>

  <ul>
    <li><code>hjkl</code> (highly recommended but not mandatory) →  basic cursor move (←↓↑→). Hint: <code>j</code> looks like a down arrow.</li>
    <li><code>:help &lt;command&gt;</code> → Show help about <code>&lt;command&gt;</code>. You can use <code>:help</code> without a <code>&lt;command&gt;</code> to get general help.</li>
  </ul>
</blockquote>

<p>Only 5 commands. That is all you need to get started.
Once these command start to become natural (maybe after day or so), you should move on to level 2.</p>

<p>But first, just a little remark about <em>Normal mode</em>.
In standard editors, to copy you have to use the <code>Ctrl</code> key (<code>Ctrl-c</code> generally).
In fact, when you press <code>Ctrl</code>, it is as if all of your keys change meaning.
Using vim in normal mode is a bit like having the editor automatically press the <code>Ctrl</code> key for you.</p>

<p>A last word about notations: </p>

<ul>
  <li>instead of writing <code>Ctrl-λ</code>, I’ll write <code>&lt;C-λ&gt;</code>.</li>
  <li>commands starting with <code>:</code> end with <code>&lt;enter&gt;</code>. For example, when I write <code>:q</code>, I mean <code>:q&lt;enter&gt;</code>.</li>
</ul>

<h2 id="nd-level----feel-comfortable">2<sup>nd</sup> Level – Feel comfortable</h2>

<p>You know the commands required for survival. 
It’s time to learn a few more commands.
These are my suggestions:</p>

<ol>
  <li>
    <p>Insert mode variations:</p>

    <blockquote>
      <ul>
        <li><code>a</code>     → insert after the cursor</li>
        <li><code>o</code>     → insert a new line after the current one</li>
        <li><code>O</code>     → insert a new line before the current one</li>
        <li><code>cw</code>    → replace from the cursor to the end of the word</li>
      </ul>
    </blockquote>
  </li>
  <li>
    <p>Basic moves</p>

    <blockquote>
      <ul>
        <li><code>0</code>         → go to the first column</li>
        <li><code>^</code>         → go to the first non-blank character of the line</li>
        <li><code>$</code>         → go to the end of line</li>
        <li><code>g_</code>         → go to the last non-blank character of line</li>
        <li><code>/pattern</code>  → search for <code>pattern</code> </li>
      </ul>
    </blockquote>
  </li>
  <li>
    <p>Copy/Paste</p>

    <blockquote>
      <ul>
        <li><code>P</code>  → paste before, remember <code>p</code> is paste after current position.</li>
        <li><code>yy</code> → copy the current line, easier but equivalent to <code>ddP</code></li>
      </ul>
    </blockquote>
  </li>
  <li>
    <p>Undo/Redo</p>

    <blockquote>
      <ul>
        <li><code>u</code> → undo</li>
        <li><code>&lt;C-r&gt;</code> → redo</li>
      </ul>
    </blockquote>
  </li>
  <li>
    <p>Load/Save/Quit/Change File (Buffer)</p>

    <blockquote>
      <ul>
        <li><code>:e &lt;path/to/file&gt;</code> →  open</li>
        <li><code>:w</code> → save</li>
        <li><code>:saveas &lt;path/to/file&gt;</code> → save to <code>&lt;path/to/file&gt;</code></li>
        <li><code>:x</code>, <code>ZZ</code> or <code>:wq</code> → save and quit (<code>:x</code> only save if necessary)</li>
        <li><code>:q!</code> → quit without saving, also: <code>:qa!</code> to quit even if there are modified hidden buffers.</li>
        <li><code>:bn</code> (resp. <code>:bp</code>) → show next (resp. previous) file (buffer)</li>
      </ul>
    </blockquote>
  </li>
</ol>

<p>Take the time to learn all of these command.
Once done, you should be able to do every thing you are able to do in other editors.
You may still feel a bit awkward. But follow me to the next level and you’ll see why vim is worth the extra work.</p>

<h2 id="rd-level----better-stronger-faster">3<sup>rd</sup> Level – Better. Stronger. Faster.</h2>

<p>Congratulation for reaching this far!
Now we can start with the interesting stuff.
At level 3, we’ll only talk about commands which are compatible with the old vi editor.</p>

<h3 id="better">Better</h3>

<p>Let’s look at how vim could help you to repeat yourself: </p>

<ol>
  <li><code>.</code> → (dot) will repeat the last command,</li>
  <li>N&lt;command&gt; → will repeat the command N times.</li>
</ol>

<p>Some examples, open a file and type:</p>

<blockquote>
  <ul>
    <li><code>2dd</code> → will delete 2 lines</li>
    <li><code>3p</code> → will paste the text 3 times</li>
    <li><code>100idesu [ESC]</code> → will write “desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu “</li>
    <li><code>.</code> → Just after the last command  will write again the 100 “desu “. </li>
    <li><code>3.</code> → Will write 3 “desu” (and not 300, how clever).</li>
  </ul>
</blockquote>

<h3 id="stronger">Stronger</h3>

<p>Knowing how to move efficiently with vim is <em>very</em> important. 
Don’t skip this section.</p>

<ol>
  <li>N<code>G</code> → Go to line N</li>
  <li><code>gg</code> → shortcut for <code>1G</code> - go to the start of the file</li>
  <li><code>G</code>  → Go to last line</li>
  <li>
    <p>Word moves:</p>

    <blockquote>
      <ol>
        <li><code>w</code> → go to the start of the following word,</li>
        <li><code>e</code> → go to the end of this word.</li>
      </ol>

      <p>By default, words are composed of letters and the underscore character.
Let’s call a WORD a group of letter separated by blank characters. 
If you want to consider WORDS, then just use uppercase characters:</p>

      <ol>
        <li><code>W</code> → go to the start of the following WORD,</li>
        <li><code>E</code> → go to the end of this WORD.</li>
      </ol>

      <img alt="Word moves example" src="/Scratch/img/blog/Learn-Vim-Progressively/word_moves.jpg">
    </blockquote>
  </li>
</ol>

<p>Now let’s talk about very efficient moves:</p>

<blockquote>
  <ul>
    <li><code>%</code>&nbsp;: Go to the corresponding <code>(</code>, <code>{</code>, <code>[</code>.</li>
    <li><code>*</code> (resp. <code>#</code>)&nbsp;: go to next (resp. previous) occurrence of the word under the cursor</li>
  </ul>
</blockquote>

<p>Believe me, the last three commands are gold.</p>

<h3 id="faster">Faster</h3>

<p>Remember about the importance of vi moves?
Here is the reason.
Most commands can be used using the following general format:</p>

<p><code>&lt;start position&gt;&lt;command&gt;&lt;end position&gt;</code></p>

<p>For example&nbsp;: <code>0y$</code> means</p>

<ul>
  <li><code>0</code> → go to the beginning of this line</li>
  <li><code>y</code> → yank from here</li>
  <li><code>$</code> → up to the end of this line</li>
</ul>

<p>We also can do things like <code>ye</code>, yank from here to the end of the word.
But also <code>y2/foo</code> yank up to the second occurrence of “foo”.</p>

<p>But what was true for <code>y</code> (yank), 
is also true for <code>d</code> (delete), <code>v</code> (visual select), <code>gU</code> (uppercase), <code>gu</code> (lowercase), etc…</p>

<h2 id="th-level----vim-superpowers">4<sup>th</sup> Level – Vim Superpowers</h2>

<p>With all preceding commands you should be comfortable using vim.
But now, here are the killer features.
Some of these features were the reason I started to use vim.</p>

<h3 id="move-on-current-line-0---g-f-f-t-t--">Move on current line: <code>0</code> <code>^</code> <code>$</code> <code>g_</code> <code>f</code> <code>F</code> <code>t</code> <code>T</code> <code>,</code> <code>;</code></h3>

<blockquote>
  <ul>
    <li><code>0</code> → go to column 0</li>
    <li><code>^</code> → go to first character on the line</li>
    <li><code>$</code> → go to the last column</li>
    <li><code>g_</code> → go to the last character on the line</li>
    <li><code>fa</code> → go to next occurrence of the letter <code>a</code> on the line. <code>,</code> (resp. <code>;</code>) will find the next (resp. previous) occurrence.</li>
    <li><code>t,</code> → go to just before the character <code>,</code>.</li>
    <li><code>3fa</code> → find the 3<sup>rd</sup> occurrence of <code>a</code> on this line.</li>
    <li><code>F</code> and <code>T</code> → like <code>f</code> and <code>t</code> but backward.
<img alt="Line moves" src="/Scratch/img/blog/Learn-Vim-Progressively/line_moves.jpg"></li>
  </ul>
</blockquote>

<p>A useful tip is: <code>dt"</code> → remove everything until the <code>"</code>.</p>

<h3 id="zone-selection-actionaobject-or-actioniobject">Zone selection <code>&lt;action&gt;a&lt;object&gt;</code> or <code>&lt;action&gt;i&lt;object&gt;</code></h3>

<p>These command can only be used after an operator in visual mode.
But they are very powerful. Their main pattern is:</p>

<p><code>&lt;action&gt;a&lt;object&gt;</code> and <code>&lt;action&gt;i&lt;object&gt;</code></p>

<p>Where action can be any action, for example, <code>d</code> (delete), <code>y</code> (yank), <code>v</code> (select in visual mode).
The object can be: <code>w</code> a word, <code>W</code> a WORD (extended word), <code>s</code> a sentence, <code>p</code> a paragraph. But also, natural character such as <code>"</code>, <code>'</code>, <code>)</code>, <code>}</code>, <code>]</code>.</p>

<p>Suppose the cursor is on the first <code>o</code> of <code>(map (+) ("foo"))</code>.</p>

<blockquote>
  <ul>
    <li><code>vi"</code> → will select <code>foo</code>.</li>
    <li><code>va"</code> → will select <code>"foo"</code>.</li>
    <li><code>vi)</code> → will select <code>"foo"</code>.</li>
    <li><code>va)</code> → will select <code>("foo")</code>.</li>
    <li><code>v2i)</code> → will select <code>map (+) ("foo")</code></li>
    <li><code>v2a)</code> → will select <code>(map (+) ("foo"))</code></li>
  </ul>
</blockquote>

<img alt="Text objects selection" src="/Scratch/img/blog/Learn-Vim-Progressively/textobjects.png">

<h3 id="select-rectangular-blocks-c-v">Select rectangular blocks: <code>&lt;C-v&gt;</code>.</h3>

<p>Rectangular blocks are very useful for commenting many lines of code.
Typically: <code>0&lt;C-v&gt;&lt;C-d&gt;I-- [ESC]</code></p>

<ul>
  <li><code>^</code> → go to start of the line</li>
  <li><code>&lt;C-v&gt;</code> → Start block selection</li>
  <li><code>&lt;C-d&gt;</code> → move down (could also be <code>jjj</code> or <code>%</code>, etc…)</li>
  <li><code>I-- [ESC]</code> → write <code>-- </code> to comment each line</li>
</ul>

<img alt="Rectangular blocks" src="/Scratch/img/blog/Learn-Vim-Progressively/rectangular-blocks.gif">

<p>Note: in Windows you might have to use <code>&lt;C-q&gt;</code> instead of <code>&lt;C-v&gt;</code> if your clipboard is not empty.</p>

<h3 id="completion-c-n-and-c-p">Completion: <code>&lt;C-n&gt;</code> and <code>&lt;C-p&gt;</code>.</h3>

<p>In Insert mode, just type the start of a word, then type <code>&lt;C-p&gt;</code>, magic…
<img alt="Completion" src="/Scratch/img/blog/Learn-Vim-Progressively/completion.gif"> </p>

<h3 id="macros--qa-do-something-q-a-">Macros&nbsp;: <code>qa</code> do something <code>q</code>, <code>@a</code>, <code>@@</code></h3>

<p><code>qa</code> record your actions in the <em>register</em> <code>a</code>. 
Then <code>@a</code> will replay the macro saved into the register <code>a</code> as if you typed it.
<code>@@</code> is a shortcut to replay the last executed macro.</p>

<blockquote>
  <p><em>Example</em></p>

  <p>On a line containing only the number 1, type this:</p>

  <ul>
    <li>
      <p><code>qaYp&lt;C-a&gt;q</code> → </p>

      <ul>
        <li><code>qa</code> start recording. </li>
        <li><code>Yp</code> duplicate this line.</li>
        <li><code>&lt;C-a&gt;</code> increment the number.</li>
        <li><code>q</code> stop recording.</li>
      </ul>
    </li>
    <li><code>@a</code> → write 2 under the 1</li>
    <li><code>@@</code> → write 3 under the 2</li>
    <li>Now do <code>100@@</code> will create a list of increasing numbers until 103.</li>
  </ul>
</blockquote>

<img alt="Macros" src="/Scratch/img/blog/Learn-Vim-Progressively/macros.gif">

<h3 id="visual-selection-vvc-v">Visual selection: <code>v</code>,<code>V</code>,<code>&lt;C-v&gt;</code></h3>

<p>We saw an example with <code>&lt;C-v&gt;</code>. 
There is also <code>v</code> and <code>V</code>.
Once the selection has been made, you can:</p>

<ul>
  <li><code>J</code> → join all the lines together.</li>
  <li><code>&lt;</code> (resp. <code>&gt;</code>) → indent to the left (resp. to the right).</li>
  <li><code>=</code> → auto indent</li>
</ul>

<img alt="Autoindent" src="/Scratch/img/blog/Learn-Vim-Progressively/autoindent.gif">

<p>Add something at the end of all visually selected lines:</p>

<ul>
  <li><code>&lt;C-v&gt;</code> </li>
  <li>go to desired line (<code>jjj</code> or <code>&lt;C-d&gt;</code> or <code>/pattern</code> or <code>%</code> etc…)</li>
  <li><code>$</code> go to the end of the line</li>
  <li><code>A</code>, write text, <code>ESC</code>.</li>
</ul>

<img alt="Append to many lines" src="/Scratch/img/blog/Learn-Vim-Progressively/append-to-many-lines.gif">

<h3 id="splits-split-and-vsplit">Splits: <code>:split</code> and <code>vsplit</code>.</h3>

<p>These are the most important commands, but you should look at <code>:help split</code>.</p>

<blockquote>
  <ul>
    <li><code>:split</code> → create a split (<code>:vsplit</code> create a vertical split)</li>
    <li><code>&lt;C-w&gt;&lt;dir&gt;</code>&nbsp;: where dir is any of <code>hjkl</code> or ←↓↑→ to change the split.</li>
    <li><code>&lt;C-w&gt;_</code> (resp. <code>&lt;C-w&gt;|</code>)&nbsp;: maximise the size of the split (resp. vertical split)</li>
    <li><code>&lt;C-w&gt;+</code> (resp. <code>&lt;C-w&gt;-</code>)&nbsp;: Grow (resp. shrink) split</li>
  </ul>
</blockquote>

<img alt="Split" src="/Scratch/img/blog/Learn-Vim-Progressively/split.gif">

<h2 id="conclusion">Conclusion</h2>

<p>That was 90% of the commands I use every day.
I suggest that you learn no more than one or two new commands per day.
After two to three weeks you’ll start to feel the power of vim in your hands.</p>

<p>Learning Vim is more a matter of training than plain memorization.
Fortunately vim comes with some very good tools and excellent documentation.
Run vimtutor until you are familiar with most basic commands.
Also, you should read this page carefully: <code>:help usr_02.txt</code>.</p>

<p>Then, you will learn about <code>!</code>, folds, registers, plugins and many other features.
Learn vim like you’d learn piano and all should be fine.</p>

<script>
// Style the keywords
$(document).ready(function() {
    $('code').css({ 'border': 'solid 1px #CCC', 'padding':'3px'});
});
</script>


                </div>
                
                

                <div id="social">
                    <div class="left">  <a href="https://twitter.com/share" class="twitter-share-button" data-via="yogsototh">Tweet</a>
       <script>!function(d,s,id){var js,fjs=d.getElementsByTagName(s)[0];if(!d.getElementById(id)){js=d.createElement(s);js.id=id;js.src="//platform.twitter.com/widgets.js";fjs.parentNode.insertBefore(js,fjs);}}(document,"script","twitter-wjs");</script>
     </div>
                    <div class="left"> <div style="height: 20px; width: 120px; display: inline-block; text-indent: 0px; margin: 0px; padding: 0px; background-color: transparent; border-style: none; float: none; line-height: normal; font-size: 1px; vertical-align: baseline; background-position: initial initial; background-repeat: initial initial;" id="___plusone_0"><iframe frameborder="0" hspace="0" marginheight="0" marginwidth="0" scrolling="no" style="position: static; top: 0px; width: 120px; margin: 0px; border-style: none; left: 0px; visibility: visible; height: 20px;" tabindex="0" vspace="0" width="100%" id="I0_1357965790621" name="I0_1357965790621" src="https://plusone.google.com/_/+1/fastbutton?bsv&amp;size=medium&amp;annotation=inline&amp;width=106&amp;hl=en-US&amp;origin=http%3A%2F%2Fyannesposito.com&amp;url=http%3A%2F%2Fyannesposito.com%2FScratch%2Fen%2Fblog%2FLearn-Vim-Progressively%2F%23&amp;ic=1&amp;jsh=m%3B%2F_%2Fscs%2Fapps-static%2F_%2Fjs%2Fk%3Doz.gapi.zh_CN.gZwqmH7BbBk.O%2Fm%3D__features__%2Fam%3DiQ%2Frt%3Dj%2Fd%3D1%2Frs%3DAItRSTNldDIlocyIVzDLbesIV-IyyCHHEw#_methods=onPlusOne%2C_ready%2C_close%2C_open%2C_resizeMe%2C_renderstart%2Concircled%2Conload&amp;id=I0_1357965790621&amp;parent=http%3A%2F%2Fyannesposito.com" allowtransparency="true" data-gapiattached="true" title="+1"></iframe></div>
    <script type="text/javascript">
      (function() {
          var po = document.createElement('script'); po.type = 'text/javascript'; po.async = true;
          po.src = 'https://apis.google.com/js/plusone.js';
          var s = document.getElementsByTagName('script')[0]; s.parentNode.insertBefore(po, s);
      })();
    </script>
     </div>
                    <div class="flush"></div>
                </div>
                <div id="choixrss">
                    <a id="rss" href="http://feeds.feedburner.com/yannespositocomen">
                        Subscribe
                    </a>
                </div>
                <div class="flush"></div>

                <div class="corps" id="comment">
                    <h2 class="first">comments</h2>

					<div id="disqus_thread"><iframe id="dsq1" data-disqus-uid="1" allowtransparency="true" frameborder="0" role="application" style="width: 100%; border: none; overflow: hidden; height: 9239px;" width="100%" src="http://disqus.com/embed/comments/?f=yannesposito&amp;t_u=http%3A%2F%2Fyannesposito.com%2FScratch%2Fen%2Fblog%2FLearn-Vim-Progressively%2F&amp;t_t=%0A%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20Learn%20Vim%20Progressively%0A%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20&amp;s_o=popular#1" scrolling="no" horizontalscrolling="no" verticalscrolling="no"></iframe><iframe id="dsq3" data-disqus-uid="3" allowtransparency="true" frameborder="0" role="application" style="width: 100%; border: none; overflow: hidden; display: none;" width="100%" src="http://mediacdn.disqus.com/1357871365/build/next-switches/client.html#3"></iframe><iframe id="dsq-indicator-north" data-disqus-uid="-indicator-north" allowtransparency="true" frameborder="0" role="application" style="width: 740px; border: none; overflow: hidden; top: 0px; min-width: 740px; max-width: 740px; position: fixed; max-height: 29px; min-height: 29px; height: 29px; display: none;" scrolling="no"></iframe><iframe id="dsq-indicator-south" data-disqus-uid="-indicator-south" allowtransparency="true" frameborder="0" role="application" style="width: 740px; border: none; overflow: hidden; bottom: 0px; min-width: 740px; max-width: 740px; position: fixed; max-height: 29px; min-height: 29px; height: 29px; display: none;" scrolling="no"></iframe></div>
        			<script type="text/javascript">
        			    /* * * CONFIGURATION VARIABLES: EDIT BEFORE PASTING INTO YOUR WEBPAGE * * */
        			    var disqus_shortname = 'yannesposito'; // required: replace example with your forum shortname

        			    /* * * DON'T EDIT BELOW THIS LINE * * */
        			    (function() {
        			        var dsq = document.createElement('script'); dsq.type = 'text/javascript'; dsq.async = true;
        			        dsq.src = 'http://' + disqus_shortname + '.disqus.com/embed.js';
        			        (document.getElementsByTagName('head')[0] || document.getElementsByTagName('body')[0]).appendChild(dsq);
        			    })();
        			</script>
        			<noscript>Please enable JavaScript to view the &lt;a href="http://disqus.com/?ref_noscript"&gt;comments powered by Disqus.&lt;/a&gt;</noscript>
        			
				</div>

                <div id="entete" class="corps_spaced">
                    <div id="liens">
                        <ul><li><a href="/Scratch/en/">Home</a></li>
<li><a href="/Scratch/en/blog/">Blog</a></li>
<li><a href="/Scratch/en/softwares/">Softwares</a></li>
<li><a href="/Scratch/en/about/">About</a></li></ul>
                    </div>
                    <div class="flush"></div>
                    <hr>
                    <div id="next_before_articles">
                        <div id="previous_articles">
                            previous entries
                            
                            <div class="previous_article">
                                <a href="/Scratch/en/blog/A-more-convenient-diff/"><span class="nicer">«</span>&nbsp;A more convenient diff</a>
                            </div>
                            
                            
                            <div class="previous_article">
                                <a href="/Scratch/en/blog/Haskell-Mandelbrot/"><span class="nicer">«</span>&nbsp;ASCII Haskell Mandelbrot</a>
                            </div>
                            
                            
                            <div class="previous_article">
                                <a href="/Scratch/en/blog/Password-Management/"><span class="nicer">«</span>&nbsp;40 character's passwords</a>
                            </div>
                            
                            
                        </div>
                        <div id="next_articles">
                            next entries
                            
                            <div class="next_article">
                                <a href="/Scratch/en/blog/programming-language-experience/">Programming Language Experience&nbsp;<span class="nicer">»</span></a>
                            </div>
                            
                            
                            <div class="next_article">
                                <a href="/Scratch/en/blog/Higher-order-function-in-zsh/">Higher order function in zsh&nbsp;<span class="nicer">»</span></a>
                            </div>
                            
                            
                            <div class="next_article">
                                <a href="/Scratch/en/blog/Yesod-excellent-ideas/">Yesod excellent ideas&nbsp;<span class="nicer">»</span></a>
                            </div>
                            
                            
                        </div>
                        <div class="flush"></div>
                    </div>
                </div>


                <div id="bottom">
                    <div>
                        <a href="https://twitter.com/yogsototh">Follow @yogsototh</a>
                    </div>
                    <div>
                        <a rel="license" href="http://creativecommons.org/licenses/by-sa/3.0/">Copyright ©, Yann Esposito</a>
                    </div>
                    <div id="lastmod">
                        Created: 08/25/2011
                        Modified: 06/05/2012
                    </div>
                    <div>
                        Entirely done with
                        <a href="http://www.vim.org">Vim</a>
                        and
                        <a href="http://nanoc.stoneship.org">nanoc</a>
                    </div>
                </div>
                <div class="clear"></div>
            </div>
        </div>
