<!-- #######  YAY, I AM THE SOURCE EDITOR! #########-->
<h1 style="color: #5e9ca0;">Android MVP Pattern</h1>
<p>&nbsp;</p>
<p>This is a simple andrid project developed using MVP pattern to achieve the clean architecture.<strong>&nbsp;</strong></p>
<p>It is based on the article by&nbsp;<a href="https://blog.mindorks.com/essential-guide-for-designing-your-android-app-architecture-mvp-part-1-74efaf1cda40#.lkml1yggq">Mindorks</a>. Refer their blog to get a clear picture about the implementation.</p>

<img src="https://github.com/rajesh-android-dev/android-mvp-base/blob/master/img/20180220_184457.gif" width = 40% height = 40%/>

<p>"<span style="color: #666699;"><em>MVP is a user interface&nbsp;<a class="mw-redirect" style="color: #666699; text-decoration: underline;" title="Architectural pattern (computer science)" href="https://en.wikipedia.org/wiki/Architectural_pattern_(computer_science)">architectural pattern</a>&nbsp;engineered to facilitate&nbsp;<a style="color: #666699; text-decoration: underline;" title="Test automation" href="https://en.wikipedia.org/wiki/Test_automation">automated</a>&nbsp;<a style="color: #666699; text-decoration: underline;" title="Unit testing" href="https://en.wikipedia.org/wiki/Unit_testing">unit testing</a>&nbsp;and improve the&nbsp;<a style="color: #666699; text-decoration: underline;" title="Separation of concerns" href="https://en.wikipedia.org/wiki/Separation_of_concerns">separation of concerns</a>&nbsp;in presentation logic:</em></span></p>
<ul>
<li><span style="color: #666699;"><em>The&nbsp;model&nbsp;is an interface defining the data to be displayed or otherwise acted upon in the user interface.</em></span></li>
<li><span style="color: #666699;"><em>The&nbsp;view&nbsp;is a passive interface that displays data (the model) and routes user commands (<a style="color: #666699; text-decoration: underline;" title="Event (computing)" href="https://en.wikipedia.org/wiki/Event_(computing)">events</a>) to the presenter to act upon that data.</em></span></li>
<li><em><span style="color: #666699;">The&nbsp;presenter&nbsp;acts upon the model and the view. It retrieves data from repositories (the model), and formats it for display in the view.</span>"</em></li>
</ul>
<p><em>source : <a href="https://en.wikipedia.org/wiki/Model%E2%80%93view%E2%80%93presenter">wikipedia</a></em></p>
<p>In a nutshell : MVP is mainly used to achieve the <strong>separation of concerns</strong> and to make the code <strong>easy to test and reusable</strong>.</p>
<h2>MVP Structure</h2>
<p style="padding-left: 30px;">MVP divides the project structure into thre major components</p>
<ol>
<li><strong>Model</strong> - Which is responsible for all the data handling operations</li>
<li><strong>View </strong>-&nbsp;&nbsp;Which is responsible for inflating the views and performing UI operations respective to the data received</li>
<li>Presenter - Which acts like a bridge between Model and View. All the business logics will be written under presenter only</li>
</ol>
<h2>How it works</h2>
<p style="padding-left: 30px;">In this section, we will go through the working structure of MVP pattern</p>
<ul>
<li>View will layout the UI for the specific page.</li>
<li>The user interactions will be send over to the Presenter, where the presenter will fetches the data from the model or perform any business logic</li>
<li>Then the Presenter will instruct the view to update the UI with corrsponding to the data provided.&nbsp;</li>
<li>Model will fetch the data required for presenter from any of the storages like Server, Database, Preference or File storage</li>
</ul>
<h2>Introduction</h2>
<p style="padding-left: 30px;">In this scection, we will understand what is a Model, View &amp; Presenter in an android project.</p>
<ul>
<li style="padding-left: 30px;">A View will be of any element with an UI like Activity, Fragment or Custom views</li>
<li style="padding-left: 30px;">A presenter is a pure java class which doesn't have any access to Android Apis</li>
<li style="padding-left: 30px;">View communicate with presenter through an interface and vice versa</li>
<li style="padding-left: 30px;">Model consists of different elements since data can be acquired from any type of source. The main part of model is Data Manager class which is connected to four helper classes namely
<ul>
<li style="padding-left: 30px;">ApiHelper (For api related calls)</li>
<li style="padding-left: 30px;">PreferenceHelper (For getting data from Shared Prefernce)</li>
<li style="padding-left: 30px;">DatabaseHelper (For getting data from local DB)</li>
<li style="padding-left: 30px;">FileHelper (For getting data from local files)</li>
</ul>
</li>
<li>Likewise View, Presenter will communicate with model through an interface</li>
</ul>
<h2>Dependencies involved</h2>
<ol>
<li><a href="https://github.com/google/dagger">Dagger2</a>&nbsp;- For dependency injection</li>
<li><a href="http://square.github.io/retrofit/">Retrofit</a>&nbsp;- For making api calls</li>
<li><a href="http://jakewharton.github.io/butterknife/">Butter Knife</a>&nbsp;- For view bindings</li>
<li><a href="https://github.com/bumptech/glide">Glide</a>&nbsp;- For Image loading</li>
<li><a href="https://developer.android.com/training/testing/espresso/index.html">Espresso</a>&nbsp;- For UI testing</li>
<li><a href="https://github.com/square/okhttp/tree/master/mockwebserver">MockWebServer</a>&nbsp;- For testing HTTP clients</li>
</ol>
