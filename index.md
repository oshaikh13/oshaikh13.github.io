---
layout: home
title: Home
---

<div id ="intro-wrapper" class="l-middle">
	<div id="intro-title-wrapper" class="intro-left">
		<h1 id="intro-title">Omar Shaikh</h1>
		<!-- <div id="intro-subtitle">
			Undergrad in the College of Computing at Georgia Tech.
		</div> -->
	</div>
	<div class="intro-left">
	<div class="intro-left">
		Hey there! I'm an undergrad in the College of Computing at <img class="intro-logo" style="width: 18px; padding-bottom: 3px;" src="/images/gt.png"> Georgia Tech (go Jackets!) I'm advised by <a href="http://www.cc.gatech.edu/~dchau/">Polo Chau</a>, working at the <a href="http://poloclub.gatech.edu">Polo Club of Data Science</a>.
	</div>
	<div style="height: 1rem"></div>
	<div>
		My interests lie at the intersection of human-computer interaction and machine learning. I'm fascinated by the amount of trust we place in computing technologies without democratizing how they work to non-experts. 
	</div>
	<div style="height: 1rem"></div>
	<div>
		Currently, I'm drawn to research that aims to identify/explain complexities to humans in intelligent systems that affect humans, especially in systems that (attempt to) understand language.
	</div>
	<div style="height: 1rem"></div>
	<div>
		I've spent a bit of time as a research intern at <img class="intro-logo" style="width: 19px; padding-bottom: 5px;" src="/images/square.svg"> Square, <img class="intro-logo" style="width: 18px; padding-bottom: 3px;" src="/images/usc.svg"> University of Southern California, and <img class="intro-logo" style="width: 24px" src="/images/cornell.svg"> Cornell University.
	</div>
</div>

<div class="intro-right">
	<img id="intro-image" class="intro-right" src="/images/portrait.png">
	<div style="height: 0.5rem"></div>
	<div id="intro-image-links" class="intro-right">
		{% for link in site.data.social-links %}
			{% if link.on-homepage == true %}
				{% include social-link.html link=link %}
			{% endif %}
		{% endfor %}
	</div>
	<div style="height: 0.5rem"></div>
	<div id="intro-cv-wrapper" class="intro-right">
		{% for link in site.data.social-links %}
			{% if link.id == "cv-web" %}
				{% include social-link.html link=link %}
			{% endif %}
		{% endfor %}
		<!-- <div id="intro-cv"><a href="/cv">Here's my CV.</a></div> -->
	</div>
	</div>
</div>

<hr class="l-middle home-hr">

<h2 class="feature-title l-middle">
	Featured <a href="/cv#publications">Research Publications</a>
</h2>
<div class="cover-wrapper l-screen">
	{% assign sortedPublications = site.categories.papers | sort: 'feature-order' %}
	{% for feature in sortedPublications %}
		{% if feature.featured == true %}
			{% include feature.html feature=feature %}
		{% endif %}
	{% endfor %}
</div>



[gt]: http://www.gatech.edu "Georgia Tech"
[cse]: http://cse.gatech.edu "Georgia Tech Computational Science and Engineering"
[coc]: http://www.cc.gatech.edu "Georgia Tech College of Computing"

[cv]: {{ site.url }}/cv
[polo]: http://www.cc.gatech.edu/~dchau/ "Polo Chau"
