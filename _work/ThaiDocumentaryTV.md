---
layout: subpage
num: 1
title: Thai Documentary TV
image: assets/images/thaidocumentary.png
description: มุ่งเน้นการส่งเสริมการดำเนินงานด้านสิ่งแวดล้อมและการพัฒนาอย่างยั่งยืนของธุรกิจต่างๆ เพื่อให้เกิดประโยชน์ร่วมกันต่อผู้มีส่วนได้เสีย เกิดเป็นสังคมที่อยู่ร่วมกันอย่างยั่งยืน ถาวร 
---

<section>
	<div class="row">
	{% for work in site.data.ThaiDocumentaryTV %}
		<div class="col-lg-4">
		<!-- <img src="{{ 'assets/images/PHimg.png' | relative_url }}" width="100%" > -->
		<a href="#" data-toggle="modal" data-target="#{{ work.youtube }}">
			<img src="https://img.youtube.com/vi/{{ work.youtube }}/0.jpg" width="100%">
			<h4>
				{{ work.name}}
			</h4>
		</a>
		{{ work.description }}<br>
		</div>

<div class="modal fade" id="{{ work.youtube }}" tabindex="-1" role="dialog" aria-labelledby="exampleModalLabel" aria-hidden="true">
	<div class="modal-dialog" role="document">
		<div class="modal-content">
			<div class="modal-header">
				<h5 class="modal-title" id="exampleModalLabel">Bangkok Impress | {{ work.name }} </h5>
				<button type="button" class="close" data-dismiss="modal" aria-label="Close">
				<span aria-hidden="true">&times;</span>
				</button>
			</div>

<div class="modal-body">
	<!-- <img src="https://img.youtube.com/vi/{{ work.youtube }}/0.jpg" width="20%"> -->
		<h4>
			{{ work.name}}
		</h4>
		<p>{{ work.description }}</p>
		<ul>	
			{% for chap in work.chaptor %}
				<li>
				<a href="https://www.youtube.com/watch?v={{ chap.youtube }}" target="_blank">
					<img src="https://img.youtube.com/vi/{{ chap.youtube }}/0.jpg" width="20%">
				{{ chap.title }}
				</a>
				<!-- {{ chap.description }}<br> -->
				</li>
			{% endfor %}
		</ul>
	
</div>

<div class="modal-footer">
	<button type="button" class="btn btn-secondary" data-dismiss="modal">Close</button>
	<!-- <button type="button" class="btn btn-primary">Send message</button> -->
</div>
		</div>
	</div>
</div>
	{% endfor %}
	</div>
	
	<!-- <div>
		{% for work in site.data.bangkokimpress %}
        	<span class="date">{{ work.name }} -</span>
            {% for chap in work.chaptor %}
            	{{ chap.title }}, {{ chap.description }} <small>({{ chap.youtube }})</small>
            {% endfor %}
            <h5>{{ work.youtube }}</h5>
            <p>{{ work.description | markdownify }}</p>
        {% endfor %}
	</div> -->
</section>

<!-- <section>
    <div class="row">
		<div class="4u 6u$(small)">
			<iframe id="ytplayer" type="text/html" 
	  		src="https://www.youtube.com/embed/jQ_vjfHTc28"
	  		frameborder="0"></iframe>
		</div>
		<div class="4u 6u$(small)">
			<iframe id="ytplayer" type="text/html" 
	  		src="https://www.youtube.com/embed/t9M5Qisg-NU?list=PLr8CA-SlIPTSALOxqe2BgUznLhzqd5HYl"
	  		frameborder="0"></iframe>
		</div>
		<div class="4u 6u$(small)">
			<iframe id="ytplayer" type="text/html" 
	  		src="https://www.youtube.com/embed/
	  		ZKNRjy1UitM"
	  		frameborder="0"></iframe>
		</div>
		<div class="4u 6u$(small)">
			<iframe id="ytplayer" type="text/html" 
	  		src="https://www.youtube.com/embed/bRsNu460v4s"
	  		frameborder="0"></iframe>
		</div>
	</div>
</section> -->