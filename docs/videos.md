---
layout: page
title: Videos
navname: Videos
permalink: /videos/
---

<h1 class="text-4xl text-gray-100 text-center pb-8 pt-4">Videos</h1>

<div id="videos-container" class="flex flex-wrap w-full justify-center items-center pb-16 lg:py-16 sm:mx-auto">
    {% for video in site.data.yt_videos.videos %}
        
        <div class="w-full sm:w-1/2 lg:w-1/3 p-2 fade-in-fwd">
            
            <div class="relative overflow-hidden rounded-lg shadow-xl" style="padding-top: 56.25%;">
                
                <iframe 
                    class="absolute top-0 left-0 w-full h-full"
                    src="https://www.youtube.com/embed/{{ video.id }}?rel=0" 
                    frameborder="0" 
                    allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" 
                    allowfullscreen>
                </iframe>
            </div>
        </div>
    {% endfor %}
</div>
