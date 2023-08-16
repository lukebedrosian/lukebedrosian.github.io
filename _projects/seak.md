---
layout: page
title: Research - SEAK Lab
description: My experience as a research assistnant in the Systems Engineering, Architecture and Knowledge Lab
img: assets/img/SEAK-Lab-Mission-1-768x432.png
importance: 1
category: experience
related_publications: seakers2022graphs
---

As a freshman seeking practical exposure in the aerospace field, I received advice from a professor about the benefits of pursuing an undergraduate [research](https://scholar.google.com/citations?user=NCYtE-8AAAAJ&hl=en&oi=ao) role. Until college, I hadn't really considered this option, but I decided to explore different aerospace professors and their areas of work. Given my strong interest in space-related activities and my dream of becoming an astronaut, I came across Dr. Daniel Selva's [Systems Engineering, Architecture and Knowledge Lab](https://www.selva-research.com/). The area of satellite technology intrigued me, leading me to join this research group.

Unbeknownst to me at the time, this experience would introduce me to a new aspect of the aerospace industry – the field of systems design and architecture. While stumbling upon this field might have been a matter of chance, my fascination with space systems design and architecture has grown significantly. As a result, I am now committed to building a career in this field.

## COMET

By far my largest undertaking in the lab, I worked under the Lockheed Martin-sponsored Comet project. The goal of this project was to develop a cognitive assistant (Siri, Alexa, GPT) that would help explore the design trade space of satellite electric power systems (EPS) in the early architecting phase.

My task was to take a set of satellite mission parameters (constant across designs) and variables to size a satellite using theoretical equations and industry-accepted parametric equations, and to then assign the design a performance metric. For example, some of the parameters were the mission lifetime and payload mass, while some of the variables were the type of battery and the number of batteries. The first step in this process was to develop a software architecture (Python) that could support this problem. I created an assortment of classes and subclasses that served specific purposes, e.g., Solar Array Design, Performance Scoring, etc. Borrowing some of the tactics from VASSAR above, I implemented a variety of theoretical and parametric equations for the preliminary sizing of the space system. For the EPS system itself, I employed more in-depth techniques of designing the subsystem. One such technique was my use of the [OrbitPy](https://github.com/EarthObservationSimulator/orbitpy) library to propogate a day-worth of orbit data. I then used this data to take the dot product of the sun vector and the normal vector to the solar array to get a higher-fidelity estimate of the array's performance. Techniques such as this and calculating more realistic inherent degradations are among a few of the techniques to get more realistic EPS estimations.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/array_equation.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

<div class="caption">
    The equation used to calculate solar array power. Note: the cosine reflects the dot product between the sun vector and normal vector
</div>

Once a satellite design was completed, a it would then output the masses of each subsystem, the overall mass, the power produced by the arrays, the battery storage, and the cost of the spacecraft. I then used a performance metric to score how well the EPS system met its requirements, namely, it was the weighted average of the power produced over the minimum required power and the battery storage over the minimum battery storage required.

I then used this design evaluator to explore the trade space with a Multi-Objective Evolutionary Algorithm. I used the [DEAP](https://deap.readthedocs.io/en/master/) library to implement an NSGA-II Genetic Algorithm with objectives of maximizing performance score and minimizing cost. I then was able to explore the pareto front and evaluate the merit of the program's outputs.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/comet_plot.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

<div class="caption">
    Example plot after running the NSGA-II.
</div>

Once I completed my design, a graduate student, [Gabriel Apaza](https://www.selva-research.com/people/gabe-apaza/), used the program as the backend of an artificial intelligence agent, Daphne, that used the evaluator to datamine and find optimal solutions. This step involved incorporating it with a nice Graphical User Interface for the user to easily specify what they were exploring within the model.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/comet_gui.jpg" title="GUI" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

<div class="caption">
    Comet GUI as implemented by Gabriel Apaza.
</div>

## VASSAR

Some of the early work I did in the lab was improving a huge program within the lab called [VASSAR](http://systemarchitect.mit.edu/docs/selva13a.pdf) -  Value Assessment of System Architectures using Rules, which was my first introduction to early, pre-Phase A mission planning and architecting. A wide variety of theoretical equations and industry-accepted parametric equations are employed in VASSAR. My first major contribution to VASSAR was implementing new design rules to include electric propulsion. In order to do this, I employed a mass and cost model for selecting thruster size in electric propulsion systems (Hofer & Randolph), where both the mass and cost model are functions of number of thrusters and system power. To obtain the power estimation, I created a database of available Hall thrusters to get a relationship between thruster power and thrust.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/table_eps.jpg" title="EPS" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/plot_eps.jpg" title="EPS" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    A table of the hall thruster attributes (left) and the curve fit (right).
</div>

I then had to use Delta-V to calculate thrust. To do this, I had to introduce a new input for the time of burn, which was based on mission parameters.

The new rules could successfully go from delta-V to thrust, then to power, and finally to mass and cost, which could be used to determine the feasibility of electric propulsion systems for the satellite mission. This was all done in Java and Jess (Clips).

## Anisomorphic Trees

For the anisomorphic trees and decision graphs project, I assisted [Dr. Ada-Rhodes Short](https://www.selva-research.com/people/ada-rhodes/) in writing the analysis and conclusion sections of the paper, which was presented at AIAA SCITECH 2022.

## Hardware-In-The-Loop Satellite Simulator

I worked on this project under the Texas A&M Undergraduate Summer Research Grant in 2022. You can find the paper here: [Paper](https://www.lukebedrosian.com/assets/pdf/satellite_simulator.pdf)

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/Poster1.jpg" title="Poster" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/seak_poster.jpg" title="Luke with Poster" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    A photo of me presenting my poster.
</div>