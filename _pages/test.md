---
permalink: /test/
title: "Test Page"
author_profile: true
redirect_from: 
  - /md/
  - /test.html
---
<html>
    <script src="https://ajax.googleapis.com/ajax/libs/jquery/1.11.3/jquery.min.js"></script>
    <script src="../assets/js/bibtex_js.js" type="text/javascript" charset="utf-8"></script>
    <bibtex src="../assets/publications.bib"></bibtex>
    
    <script>
		$(function() {
		  $("#Fontselector").on("change",function() {
		    var font = $("#Fontselector option:selected").text();
		    console.log(font);
		
		    $('.title.fonters').each(function() {
		    	$(this).css("font-family",font);
		    });
		  }); 
		});
		function reset() {
			$("select").each(function () {
			  localStorage.setItem($(this).attr("id"),"");
			  $(this).val("");
			}); 
			$("#searchbar").val("");
			$("#searchbar").trigger('change');
		}
    </script>
    
    <!-- Latest compiled and minified CSS -->
    <link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.5/css/bootstrap.min.css">

<div class="container-fluid">
	<div class="searchbar">
		<div style="float:left;">
			<select id="authorselectfirst" class="btn bibtex_search bibtex_author" style="border: 1px solid lightgrey;" extra="first" search="author">
			  <option value="">Search First Author</option>
			</select>
		</div>
		<div style="float:left;">
			<select id="authorselect" class="btn bibtex_search bibtex_author" style="border: 1px solid lightgrey;" search="author">
			  <option value="">Search Author</option>
			</select>
		</div>
		<div style="float:left;">
			<select id="topicselect" class="btn
							bibtex_search"
				style="border: 1px solid lightgrey;" search="topic">
			  <option value="">Search Topic</option>
			  <!-- Add topic values here -->
			  <option value="test1">Test1</option>
			  <option value="test2">Test2</option>
			  <option value="Autonomy">Autonomy</option>
			  <option value="Symbiotic">Symbiotic Autonomy</option>
			  <option value="CoBot|Episodic|Service|Insights|Model-Instance|Diverse">CoBot</option>
			  <option value="Learning">Learning</option>
			  <option value="Multiagent">Multiagent Systems</option>
			  <option value="Multi-robot|Multirobot|soccer|Multiagent">Multirobot Systems</option>
			  <option value="Planning">Planning</option>
			  <option value="Robot">Autonomous Robots</option>
			  <option value="Localization">Robot Localization</option>
			  <option value="Soccer|Multi-robot">Robot Soccer</option>
			  <option value="Vision">Vision</option>
			</select>
		</div>
		<br/><br/>
		<div style="float:left;">
			<button type="button" class="btn bibtex_search" onclick="reset()">Reset</button>
		</div>
		<div style="float:left;">
			<input type="text" class="bibtex_search form-control" id="searchbar" placeholder="Search publications">
			<span class="help-block">Example: journal 2015 (finds the intersection of the two terms)</span>
		</div>
		
	</div>
</div>

<div class="bibtex_structure">
  <div class="group year" extra="ASC number">
  	  <a href="#top" style="display: inline"><em>(Top of the page)</em></a>
  	  <div style="padding-bottom:10px;"></div>
  	  <div class="sort journal" extra="DESC string">
      	<div class="templates"></div>
      </div>
  </div>
</div>

<div id="bibtex_display">

  <div class="if bibtex_template" style="display: none;">
    <ul> <li>
      <span class="if journal !nolink">
        <a class="bibtexVar" href="http://www.cs.cmu.edu/~mmv/papers/+BIBTEXKEY+.pdf" extra="BIBTEXKEY">
            <span style="text-decoration: underline;" class="title"></span>,
        </a>
      </span>
      <span class="if title nolink">
            <span class="title"></span>,
      </span>
      <div class="if author">
        <span class="author"></span>
      </div>
      <div>
        <span class="if journal"><em><span class="journal"></span></em>,</span>
        <span class="if booktitle">In <em><span class="booktitle"></span></em>,</span>
        <span class="if editor"><span class="editor"></span> (editors),</span>
        <span class="if publisher"><em><span class="publisher"></span></em>,</span>
        <span class="if !journal number">Technical report <span class="number"></span>,</span>
        <span class="if institution"><span class="institution"></span>,</span>
        <span class="if address"><span class="address"></span>,</span>
        <span class="if volume"><span class="volume"></span>,</span>
        <span class="if journal number">(<span class="number"></span>),</span>
        <span class="if pages"> pages <span class="pages"></span>,</span>
        <span class="if month"><span class="month"></span>,</span>
        <span class="if year"><span class="year"></span>.</span>
        <span class="if note"><span class="note"></span>.</span>
        <a class="bibtexVar" role="button" data-toggle="collapse" href="#bib+BIBTEXKEY+" aria-expanded="false" aria-controls="bib+BIBTEXKEY+" extra="BIBTEXKEY">
		  [bib]
		</a>
      </div>
      <div class="bibtexVar collapse" id="bib+BIBTEXKEY+" extra="BIBTEXKEY">
		  <div class="well">
		    <pre><span class="bibtexraw noread"></span></pre>
		  </div>
	  </div>
      <div style="display:none"><span class="bibtextype"></span></div>
      <div style="display:none"><span class="if topic"><span class="topic"></span></span></div>
    </li></ul>
  </div>
  
</div>
<!-- Latest compiled and minified JavaScript -->
<script src="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.5/js/bootstrap.min.js"></script>

<br/>This publication page is generated by using <a href = "https://github.com/pcooksey/bibtex-js">bibtex_js</a>.
</html>
