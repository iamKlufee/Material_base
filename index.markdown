---
layout: default
title: Home
---

<section class="hero-section">
    <div class="container">
        <h2>High-Quality Resources for Your Research & Visualizations</h2>
        <p class="lead">Access a curated library of free vector graphics and 3D models designed for academic papers, presentations, and scientific illustrations.</p>
        <div class="d-grid gap-2 d-md-flex justify-content-center">
            <a href="{{ '/vectors/' | relative_url }}" class="btn btn-primary btn-lg">Explore Vectors</a>
            <a href="{{ '/3d_models/' | relative_url }}" class="btn btn-outline-light btn-lg">Browse 3D Models</a>
        </div>
    </div>
</section>

{% include google_adsense.html %} {# Google AdSense slot #}

<section class="latest-materials mb-5">
    <h3 class="mb-4 text-center">Featured Resources</h3>
    <div class="row row-cols-1 row-cols-md-3 g-4">
        {% for vector in site.vectors limit:3 %}
        <div class="col">
            <div class="card material-card h-100">
                <img src="{{ vector.thumbnail | relative_url }}" class="card-img-top" alt="{{ vector.title }}">
                <div class="card-body">
                    <h5 class="card-title"><a href="{{ vector.url | relative_url }}">{{ vector.title }}</a></h5>
                    <p class="card-text">{{ vector.description | truncate: 100 }}</p>
                    <a href="{{ vector.download_link | relative_url }}" class="btn btn-primary btn-sm mt-auto">Download</a>
                </div>
            </div>
        </div>
        {% endfor %}
        {% for model in site.3d_models limit:3 %}
        <div class="col">
            <div class="card material-card h-100">
                <img src="{{ model.thumbnail | relative_url }}" class="card-img-top" alt="{{ model.title }}">
                <div class="card-body">
                    <h5 class="card-title"><a href="{{ model.url | relative_url }}">{{ model.title }}</a></h5>
                    <p class="card-text">{{ model.description | truncate: 100 }}</p>
                    <a href="{{ model.download_link | relative_url }}" class="btn btn-primary btn-sm mt-auto">Download</a>
                </div>
            </div>
        </div>
        {% endfor %}
    </div>
</section>

<section class="how-it-works text-center my-5">
    <h3>How It Works</h3>
    <p>We provide high-quality assets. Simply browse, download, and integrate into your work.</p>
    <div class="row mt-4">
        <div class="col-md-4">
            <div class="p-3 bg-white shadow-sm rounded h-100">
                <h4>1. Explore</h4>
                <p>Browse our extensive library of vectors and 3D models categorized for easy discovery.</p>
            </div>
        </div>
        <div class="col-md-4">
            <div class="p-3 bg-white shadow-sm rounded h-100">
                <h4>2. Download</h4>
                <p>Select your desired asset and download it instantly, completely free of charge.</p>
            </div>
        </div>
        <div class="col-md-4">
            <div class="p-3 bg-white shadow-sm rounded h-100">
                <h4>3. Integrate</h4>
                <p>Use our resources in your research papers, presentations, educational materials, and more.</p>
            </div>
        </div>
    </div>
</section>