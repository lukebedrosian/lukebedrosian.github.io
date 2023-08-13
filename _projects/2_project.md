---
layout: page
title: Exploring - Summer 2023
description: A look into what I've explored during the summer of 2023.
img: assets/img/elsegundo.jpg
importance: 1
category: fun
related_publications: einstein1956investigations, einstein1950meaning
---

As a self-proclaimed philomath, I take pride in my learning endeavors. I have a genuine passion for learning and am interested
in a variety of subjects. This page summarizes some of my current pursuits in the summer of 2023.

**Artificial Intelligence: A Modern Approach**

I've recently started reading and working through the textbook *Artificial Intelligence: A Modern Approach*, by Stuart Russell and Peter Norvig.
My interests in artificial intelligence first sprouted whilst working in my research lab, the Systems Engineering, Architecture and Knowledge (SEAK) Lab, under Dr. Daniel Selva Valero, Ph.D. I worked on a project called "COMET," which was sponsored by Lockheed-Martin, where I developed the backend of a cognitive assistant (think Siri) which was designed to find optimal solutions for satellite Electric Power Systems (EPS). While I did not work directly on the AI side of the project and was more focused on the satellite design rules, evaluator function and optimization techniques (MOEA, NSGA-II), I had a great fascination with the concept of AI, and was delighted to see my work being utilized by an intelligent agent. My interest was further sparked after attending the AIAA Intelligent Systems workshop at Texas A&M in the summer of 2022, where researchers from across the country spoke on intelligent systems and their application to the space industry. I intend on gaining a solid foundation in artificial intelligence by digesting this book and applying its teachings to personal projects, my academic research and future work.


**Crucial Conversations**

Another book I'm currently devouring is *Crucial Conversations* by Grenny et al. This work breaks down the art of having crucial conversations, which are conversations when stakes are high, opinions vary, and emotions start to run strong. My mentor at The Aerospace Corporation, where I am interning this summer, recommended this book. The ability to handle crucial conversations - correctly, that is - enables one to achieve greater success in our companies, careers, communities, relationships, personal health, etc. Already, this book flipped my worldview upside-down, and I'm excited to apply what I learn to all aspects of my life.

**Outlive**

I've followed Dr. Peter Attia, MD, for a while now. I first encountered his podcast, "The Drive," in the summer of 2021, and have been an avid listener since. Attia specializes in the practice of longevity, which is maximizing both lifespan (length of life) and healthspan (quality of life). When I learned Dr. Attia was releasing his book, *Outlive,* I immediately preordered it. Thusfar, this book lays the foundation for maximizing one's longevity in a very methodical way. I especially appreciate his understanding of risk and the mathematics (he did an engineering undergrad) behind death and suffering. I recommend this book to anybody that cares about their health and want to make methodical, impactful changes for the better.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/ai.jpg" title="Artificial Intelligence: A Modern Approach" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/crucial.jpg" title="Crucial Conversations" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/outlive.jpg" title="Outlive" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Book covers of the three books discussed above.
</div>
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/5.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    This image can also have a caption. It's like magic.
</div>

You can also put regular text between your rows of images.
Say you wanted to write a little bit about your project before you posted the rest of the images.
You describe how you toiled, sweated, *bled* for your project, and then... you reveal its glory in the next row of images.


<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.html path="assets/img/6.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-4 mt-3 mt-md-0">
        {% include figure.html path="assets/img/11.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    You can also have artistically styled 2/3 + 1/3 images, like these.
</div>


The code is simple.
Just wrap your images with `<div class="col-sm">` and place them inside `<div class="row">` (read more about the <a href="https://getbootstrap.com/docs/4.4/layout/grid/">Bootstrap Grid</a> system).
To make images responsive, add `img-fluid` class to each; for rounded corners and shadows use `rounded` and `z-depth-1` classes.
Here's the code for the last row of images above:

{% raw %}
```html
<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.html path="assets/img/6.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-4 mt-3 mt-md-0">
        {% include figure.html path="assets/img/11.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
```
{% endraw %}
