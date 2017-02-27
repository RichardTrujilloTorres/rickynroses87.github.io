---
# You don't need to edit this file, it's empty on purpose.
# Edit theme's home layout instead if you wanna make some changes
# See: https://jekyllrb.com/docs/themes/#overriding-theme-defaults
layout: default
title: Home
---



<div class="section">
   <div class="container">
       <h2 class="section-title">Entries</h2>

        <div class="row">


        {% for post in site.posts %}

       


            <div class="col-md-4">
                <div class="card card-plain">
                    <div class="image">
                        <img src="{{ post.image_url | absolute_url }}" alt="...">
                        <div class="filter">
                            <a href="{{ post.url }}" class="btn btn-neutral btn-simple">
                                <i class="fa fa-align-left"></i> Read article
                            </a>
                        </div>
                    </div>
                    <div class="content">
                        <p class="category text-info">
                                 {{ post.category }}
                        </p>
                        <a class="card-link" href="{{ post.url }}">
                            <h4 class="title">{{ post.title }} </h4>
                        </a>

                         <div class="footer">

                             <div class="stats pull-right">
                                 <a class="card-link" href="#">
                                    <i class="fa fa-calendar"></i> 
                                    {{ post.date | date: "%d %B %Y" }}
                                 </a>
                            </div>

                        </div>


                    </div>
                </div> <!-- end card -->
            </div>


        {% endfor %}

       </div>
   </div>
</div><!-- section -->