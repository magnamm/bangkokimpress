---
layout: subpage
num: 2
title: Bangkok Impress
image: assets/images/bangkok impress final.png
description: หน่วยงานหนึ่งที่สำคัญต่อการผลิตสื่อสร้างสรรค์อย่างมีคุณภาพ โดยมีพันธกิจหลัก คือ การผลิตสารคดี รายการโทรทัศน์  วิดีทัศน์  และสื่อสิ่งพิมพ์  ที่มีเนื้อหาสาระอันดีงามด้านศาสนาและวัฒนธรรม ก่อให้เกิดประโยชน์สุขต่อสังคม และประเทศชาติ 
---

<section>
	<div class="row">
	{% for work in site.data.bangkokimpress %}
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
<!-- 
<a href="#" data-toggle="modal" data-target="#exampleModal" data-whatever="@mdo">Open modal for @mdo</a>
<a href="#" data-toggle="modal" data-target="#exampleModal" data-whatever="@fat">Open modal for @fat</a>
<a href="#" data-toggle="modal" data-target="#exampleModal" data-whatever="@getbootstrap">Open modal for @getbootstrap</a>
 -->
<!-- 
<div class="modal fade" id="exampleModal" tabindex="-1" role="dialog" aria-labelledby="exampleModalLabel" aria-hidden="true">
  <div class="modal-dialog" role="document">
    <div class="modal-content">
      <div class="modal-header">
        <h5 class="modal-title" id="exampleModalLabel">Bangkok Impress</h5>
        <button type="button" class="close" data-dismiss="modal" aria-label="Close">
          <span aria-hidden="true">&times;</span>
        </button>
      </div>
      <div class="modal-body">
        ...
      </div>
      <div class="modal-footer">
        <button type="button" class="btn btn-secondary" data-dismiss="modal">Close</button>
        <button type="button" class="btn btn-primary">Send message</button>
      </div>
    </div>
  </div>
</div> -->