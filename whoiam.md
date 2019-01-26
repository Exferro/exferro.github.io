---
layout: page
title: Who I Am
image_path: "/public/img/whoiam"
image_num: 5
images:
 - url: "/me_yachting.jpg"
   idx: 1
   caption: "Me and sails"
 - url: "/ivan_ivanovich.jpg"
   idx: 2
   caption: "Ivan Kazachek, our Physics tutor"
 - url: "/viktor_fedorovich.jpg"
   idx: 3
   caption: "Viktor Sannikov, our Math tutor"
 - url: "/yft_odessa.jpg"
   idx: 4
   caption: "Ukraine Young Physics Tournament. Odessa, November 2011"
 - url: "/last_summer.jpg"
   idx: 5
   caption: "Photo before leaving the school. Ivan Ivanovich says that an ability to integrate at school doesn't represent one's mental qualities. But of course, it makes one much <b>cooler</b>, so he may use sign of the horns at any moment. We were in one step from attending the university, so we decided hands full of \"horns\" would be the right option to show our expectations!"


---
It was Saturday and my eighth year at school had just began. I was going to the first lesson of elective on Physics. I wasn't really in the mood — month before that I had started visiting sailing lessons — of course, I would have preferred to spend another September evening with staysails and spinnakers! Moreover, I had already visited several lessons of Math elective and they weren't a pleasure trip, not in a tiny bit — they were bringing my mind to new levels with the price of headache.

Nevertheless, my Mom insisted that I had attended at least first lesson on Physics, just to compare. I obeyed, what else could I have done.

That changed **everything** (Mom, thank you!).

Supposedly boring lessons turned out to be a great time of curiosity, discoveries and a wit. It was Ivan Ivanovich, our Physics tutor, who lead us through the adventurous and bright world of Physics, full of its unique humor. 

(Not to offend anybody, I shall mention that Math lessons were incredible as well, but they were distinct — more rigorous. I guess, it was the first time when I realized the difference between Physics and Math: the former strives to think of everything as simple as possible, while the latter does the opposite.)

### What was next?

Well, we were not just studying Physics, Math and Computer Science (one more elective I started to attend) — we were involved into them with the best possible way for pupils — we participated in olympiades and tournaments! I remember that time with a great pleasure, for I visited then different cities of Ukraine — North and South, West and East — and everywhere a great spirit of competition intertwined (or, may I say, *entangled*) with a warm atmosphere of friendship and a great ambience of Science. 

And, of course, there were a constant presence of the legendary Phystech in our minds. It was a Great Dream to study at the best Russian  university 

<!-- Slideshow container -->
<div class="slideshow-container">

	{% assign images = page.images %}
 	{% for image in page.images %}
 		<div class="mySlides fade">
			<div class="numbertext"> {{ image.idx}} / {{ page.image_num }}</div>
			<img src="{{ page.image_path }}{{ image.url }}" style="height:17em; display: block; margin-left: auto;  margin-right: auto; ">    
		</div>
 	{% endfor %}

  <!-- Next and previous buttons -->
  <a class="prev" onclick="plusSlides(-1)">&#10094;</a>
  <a class="next" onclick="plusSlides(1)">&#10095;</a>
</div>

<div style="text-align:center">
	{% assign images = page.images %}
	{% for image in page.images %}
		<div class="caption">{{ image.caption }}</div> 
	{% endfor %}
</div>

<!-- The dots/circles -->
<div style="text-align:center">
	{% assign images = page.images %}
	{% for image in page.images %}
		<span class="dot" onclick="currentSlide({{ image.idx }})"></span> 
	{% endfor %}
</div>
<br>

<script>
var slideIndex = 1;
showSlides(slideIndex);

function plusSlides(n) {
  showSlides(slideIndex += n);
}

function currentSlide(n) {
  showSlides(slideIndex = n);
}

function showSlides(n) {
  var i;
  var slides = document.getElementsByClassName("mySlides");
  var captions = document.getElementsByClassName("caption")
  var dots = document.getElementsByClassName("dot");
  if (n > slides.length) {slideIndex = 1}    
  if (n < 1) {slideIndex = slides.length}
  for (i = 0; i < slides.length; i++) {
      slides[i].style.display = "none";  
  }
  for (i = 0; i < slides.length; i++) {
      captions[i].style.display = "none";  
  }
  for (i = 0; i < dots.length; i++) {
      dots[i].className = dots[i].className.replace(" dot_active", "");
  }
  slides[slideIndex-1].style.display = "block";  
  captions[slideIndex-1].style.display = "block"; 
  dots[slideIndex-1].className += " dot_active";
}
</script>

