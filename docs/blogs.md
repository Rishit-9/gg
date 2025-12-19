---
layout: page
title: Our Blogs
permalink: /blogs/
navname: Blogs
---

<div class="py-8">
    <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
        {% for post in site.posts %}
        <a href="{{ site.baseurl }}{{ post.url }}" class="group block no-underline">
            <div class="bg-gray-800 rounded-xl overflow-hidden shadow-2xl transition-all duration-300 transform group-hover:-translate-y-2 group-hover:shadow-green-900/20 border border-gray-700 group-hover:border-green-500">
                <div class="h-48 bg-cover bg-center" style="background-image: url('{{ site.baseurl }}/{{ post.image }}');">
                    <div class="w-full h-full bg-black opacity-20 group-hover:opacity-0 transition-opacity"></div>
                </div>
                
                <div class="p-6">
                    <span class="text-xs font-bold text-green-400 uppercase tracking-widest">{{ post.date | date: "%B %d, %Y" }}</span>
                    <h3 class="text-xl font-bold text-white mt-2 mb-3 group-hover:text-green-400 transition-colors">{{ post.title }}</h3>
                    <p class="text-gray-400 text-sm leading-relaxed line-clamp-3">
                        {{ post.excerpt | strip_html | truncatewords: 25 }}
                    </p>
                    <div class="mt-4 flex items-center text-green-500 font-bold text-sm">
                        Read Story <span class="ml-2 transition-transform group-hover:translate-x-2">→</span>
                    </div>
                </div>
            </div>
        </a>
        {% endfor %}
    </div>
</div>

<style>
/* Custom utility for clamping text lines */
.line-clamp-3 {
    display: -webkit-box;
    -webkit-line-clamp: 3;
    -webkit-box-orient: vertical;  
    overflow: hidden;
}
</style>
