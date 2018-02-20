<!-- #######  YAY, I AM THE SOURCE EDITOR! #########-->
<h1 style="color: #5e9ca0;">Android MVP Pattern</h1>
<p>&nbsp;</p>
<p>This is a simple andrid project developed using MVP pattern to achieve the clean architecture.<strong>&nbsp;</strong></p>
<p>It is based on the article by&nbsp;<a href="https://blog.mindorks.com/essential-guide-for-designing-your-android-app-architecture-mvp-part-1-74efaf1cda40#.lkml1yggq">Mindorks</a>. Refer their blog to get a clear picture about the implementation.</p>
<p>&nbsp;</p>
<p><img src="https://media.giphy.com/media/l2hhLijQaODHvIBYoJ/giphy.gif" /></p>
<p>&nbsp;</p>
<p>"<span style="color: #666699;"><em>MVP is a user interface&nbsp;<a class="mw-redirect" style="color: #666699; text-decoration: underline;" title="Architectural pattern (computer science)" href="https://en.wikipedia.org/wiki/Architectural_pattern_(computer_science)">architectural pattern</a>&nbsp;engineered to facilitate&nbsp;<a style="color: #666699; text-decoration: underline;" title="Test automation" href="https://en.wikipedia.org/wiki/Test_automation">automated</a>&nbsp;<a style="color: #666699; text-decoration: underline;" title="Unit testing" href="https://en.wikipedia.org/wiki/Unit_testing">unit testing</a>&nbsp;and improve the&nbsp;<a style="color: #666699; text-decoration: underline;" title="Separation of concerns" href="https://en.wikipedia.org/wiki/Separation_of_concerns">separation of concerns</a>&nbsp;in presentation logic:</em></span></p>
<ul>
<li><span style="color: #666699;"><em>The&nbsp;model&nbsp;is an interface defining the data to be displayed or otherwise acted upon in the user interface.</em></span></li>
<li><span style="color: #666699;"><em>The&nbsp;view&nbsp;is a passive interface that displays data (the model) and routes user commands (<a style="color: #666699; text-decoration: underline;" title="Event (computing)" href="https://en.wikipedia.org/wiki/Event_(computing)">events</a>) to the presenter to act upon that data.</em></span></li>
<li><em><span style="color: #666699;">The&nbsp;presenter&nbsp;acts upon the model and the view. It retrieves data from repositories (the model), and formats it for display in the view.</span>"</em></li>
</ul>
<p><em>source : <a href="https://en.wikipedia.org/wiki/Model%E2%80%93view%E2%80%93presenter">wikipedia</a></em></p>
<p>In a nutshell : MVP is mainly used to achieve the <strong>separation of concerns</strong> and to make the code <strong>easy to test and reusable</strong>.</p>
<p>&nbsp;</p>
<h2>Third party libraries used</h2>
<ol>
<li><a href="https://github.com/google/dagger">Dagger2</a>&nbsp;- For dependency injection</li>
<li><a href="http://square.github.io/retrofit/">Retrofit</a>&nbsp;- For making api calls</li>
<li><a href="http://jakewharton.github.io/butterknife/">Butter Knife</a>&nbsp;- For view bindings</li>
<li><a href="https://github.com/bumptech/glide">Glide</a>&nbsp;- For Image loading</li>
<li><a href="https://developer.android.com/training/testing/espresso/index.html">Espresso</a>&nbsp;- For UI testing</li>
<li><a href="https://github.com/square/okhttp/tree/master/mockwebserver">MockWebServer</a>&nbsp;- For testing HTTP clients</li>
</ol>
