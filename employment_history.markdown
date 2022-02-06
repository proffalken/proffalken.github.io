---
title: Employment History
permalink: /employment_history/
icon: nc-bank
order: 1
---

<div class="row">
<div class="col-md-12">
<h3 class="description">What's the TL;DR?</h3>
</div>
</div>
<div class="row">
<div class="col">
<p>There's been a few jobs over the years, so I don't blame you for wanting a quick summary.</p>
<p>I've spent almost all of the past 21 years working in the IT industry and, having started straight from leaving school, I've worked at all levels from first-line tech support through to running my own businesses, including working for some of the best DevOps consultancies in the UK.</p>
<p>I'm currently at <A href="https://contino.io/">Contino</a> where I'm advising some of the UK's favourite household brands on their observability strategies and helping them build out their cloud capabilities, but it's not always been Infrastructure as Code and SRE!</p>
<p>One of the major roles I've held in my career was that of Cluster Manager at Namesco.  Responsible for a significant budget and the leadership of a small team of engineers, it was our job to ensure that over half a million websites and all their associated databases, mailboxes, and domains stayed online.</p>
<p>This was before "The Cloud" was really a thing, so there were many late nights in datacentres installing equipment into racks, testing connectivity between sites, and configuring large-scale storage devices such as NetApps. Don't tell anyone, but there are days when I really miss being able to actually pick up a server and take it apart to fix it instead of just provisioning a new instance in AWS!</p>
<p>I've also got experience of designing, deploying, and managing a complete sensor-to-dashboard IoT solution using LoRaWAN as the data transport, with the platform being used to monitor everything from schools through to vineyards, and air quality to agricultural vehicle movements.</p>
</div>
</div>
<div class="row">
<div class="col-md-12">
<h3 class="description">Career Overview</h3>
</div>
</div>
<div class="row">
<div class="col">
<p>Here's a list of all the roles I've held to date, along with a summary of each of them.</p>
<p>If you're looking for some of the other projects that I've worked on, then where I'm allowed to I've documented them <a href="/projects">here</a>.</p>
</div>
</div>
{% for role in site.data.roles %}
<div class="row justify-content-center">
  <div class="col-md-8">
    <div class="card card-stats">
      <div class="card-header">
        <h3 class="card-title">{{ role.title }} - {{ role.company }}</h3>
      </div>
      <div class="card-body">
        <p class="card-body">{{ role.summary }}</p>
          <div class="row">
            <div class="col">
              <h5 class="text-muted">Key Technologies</h5>
              <ul class="list-group list-group-flush">
                {% for tech in role.technologies_used %}
                  <li class="list-group-item">{{ tech }}</li>
                {% endfor %}
              </ul>
            </div>
            <div class="col">
              <h5 class="text-muted">Soft Skills</h5>
              <ul class="list-group list-group-flush">
              {% for skill in role.soft_skills %}
              <li class="list-group-item">{{ skill }}</li>
              {% endfor %}
              </ul>
            </div>
          </div>
      </div>
    </div>
  </div>
</div>
{% endfor %}
