---
layout: post
title: laboratorium4
---


<h1>Laboratorium 4</h1>




<ul class="posts">
<li>
<p>1.Wyświetl listę plików z aktualnego katalogu, zamieniając wszystkie małe litery na duże.
<br/>
<div class="transbox">
ls | tr [:lower:] [:upper:]
<br/>
DESKTOP<br/>
ETC<br/>

MAIL<br/>
PUBLIC_GIT<br/>
PUBLIC_HTML<br/>
TMP<br/>
WSTEP_PROG
</div>
</p>
<br/>

<p>2.Wyświetl listę praw dostępu do plików w aktualnym katalogu, ich rozmiar i nazwę.
<br/>
<div class="transbox">
ls -l

</div>

</p>
<br/>


<p>3.Wyświetl listę plików w aktualnym katalogu, posortowaną według rozmiaru pliku.
<br/>
<div class="transbox">
 ls --sort=size -1
</div>
</p>
<br/>


<p>4.Wyświetl zawartość pliku <em>/etc/passwd</em> posortowaną według numerów UID w kolejności od największego do najmniejszego.
<br/>
<div class="transbox">
 cat /etc/passwd | sort -r -t: -g -k 3

</div>
</p>
<br/>


<p>5.Wyświetl zawartość pliku <em>/etc/passwd</em> posortowaną najpierw według numerów GID w kolejności od największego do najmniejszego, a następnie UID
<br/>
<div class="transbox">
 cat /etc/passwd | sort --field-separator=":" --general-numeric-sort --key 4,3 --reverse
</div>
</p>
<br/>


<p>6. Podaj liczbę plików każdego użytkownika.
<br/>
<div class="transbox">
...
</div>
</p>
<br/>


<p>7. Sporządź statystykę praw dostępu (dla każdego z praw dostępu
podaj ile razy zostało ono przydzielone).
<div class="transbox">
$ find -printf "%m\n" | sort | uniq -c
<br/>
     49 444<br/>
     17 600<br/>

      1 640<br/>
    159 644<br/>
      2 666<br/>
    237 700<br/>
      2 711<br/>
    658 744<br/>

    237 755<br/>
      4 777
</div>
</p>
<br/>

<p>Czy potrafisz odpowiedzieć jaki będzie efekt wykonania poniższych
poleceń?</p>

<pre class="dawn">ls -l <span class="Keyword">&gt;</span> lsout.txt                          <span class="Comment"><span class="Comment">#</span>  1</span>

ls -la <span class="Keyword">&gt;&gt;</span> lsout.txt                        <span class="Comment"><span class="Comment">#</span>  2</span>

ps <span class="Keyword">&gt;&gt;</span> psout.txt                            <span class="Comment"><span class="Comment">#</span>  3</span>
free -m <span class="Keyword">&gt;&gt;</span> <span class="Keyword">~</span>/wynik                         <span class="Comment"><span class="Comment">#</span>  4</span>

kill -1 1234 <span class="Keyword">&gt;</span> killout.txt <span class="Keyword">2&gt;</span>killerr.txt   <span class="Comment"><span class="Comment">#</span>  5</span>

kill -1 1234 <span class="Keyword">&gt;</span> killout.txt <span class="Keyword">2&gt;&amp;1</span>            <span class="Comment"><span class="Comment">#</span>  6</span>

kill -1 1234 <span class="Keyword">&gt;</span> /dev/null <span class="Keyword">2&gt;&amp;1</span>              <span class="Comment"><span class="Comment">#</span>  7</span>

sort psout.txt <span class="Keyword">&gt;</span> pssort.txt                <span class="Comment"><span class="Comment">#</span>  8</span>

ps <span class="Keyword">|</span> sort <span class="Keyword">&gt;</span> pssort.txt                     <span class="Comment"><span class="Comment">#</span>  9</span>

cat lsout.txt <span class="Keyword">|</span> sort <span class="Keyword">&gt;</span> lssort.txt          <span class="Comment"><span class="Comment">#</span> 10</span>

who <span class="Keyword">|</span> sort <span class="Keyword">|</span> more                          <span class="Comment"><span class="Comment">#</span> 11</span>

who <span class="Keyword">|</span> sort <span class="Keyword">|</span> less                          <span class="Comment"><span class="Comment">#</span> 12</span>

</pre>


</li>
</ul>

