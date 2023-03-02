---
layout: blog
permalink: /chili-con-carne-fix/
pagedesc: Chili Con Carne-Fix
title: Chili Con Carne-Fix
headline: Chili Con Carne-Fix
thumbnail: /wp-content/images/chili-con-carne-fix.webp
tags: [Fix, Gewürz]
portionen: 6-8
gesamtzeitaufwand: 1-2 Minuten
zeitaufwandzubereitung: 1-2 Minuten
htmlbeforeheadend: blog/htmlbeforeheadend.html
htmlbeforebodyend: blog/htmlbeforebodyend.html
---
<section data-bs-version="5.1">
    <div style="max-width: 600px; margin: auto; font-size: 120%; line-height: 200%;">
        <div style="margin-bottom: 20px;">
            <ul class="nav nav-tabs" id="myTab" role="tablist" style="list-style-type: none;">
                <li class="nav-item" role="presentation">
                    <button class="nav-link active" id="info-tab" data-bs-toggle="tab" data-bs-target="#rezeptinfo-tab-pane" type="button" role="tab" aria-controls="rezeptinfo-tab-pane" aria-selected="true">Rezeptinfos</button>
                </li>
                <li class="nav-item" role="presentation">
                    <button class="nav-link" id="zutaten-tab" data-bs-toggle="tab" data-bs-target="#zutaten-tab-pane" type="button" role="tab" aria-controls="zutaten-tab-pane" aria-selected="false">Zutaten</button>
                </li>
                <li class="nav-item" role="presentation">
                    <button class="nav-link" id="zubereitung-tab" data-bs-toggle="tab" data-bs-target="#zubereitung-tab-pane" type="button" role="tab" aria-controls="zubereitung-tab-pane" aria-selected="false">Zubereitung</button>
                </li>
            </ul>
            <div class="tab-content" id="myTabContent">
                <div class="tab-pane fade show active" id="rezeptinfo-tab-pane" role="tabpanel" aria-labelledby="home-tab" tabindex="0">
                    <!-- Rezeptinfo START -->
                    {% if  page.portionen %}
                        <b><i class="fa-solid fa-pizza-slice"></i> Portionen: <span class="badge bg-primary">{{ page.portionen }}</span><br></b>
                    {% endif %}
                    {% if page.gesamtzeitaufwand %}
                        <b><i class="fa-solid fa-hourglass-end"></i> Gesamtzeitaufwand:  <span class="badge bg-primary">{{ page.gesamtzeitaufwand }}</span></b>
                    {% endif %}
                    <!-- Rezeptinfo ENDE -->
                </div>
                <div class="tab-pane fade" id="zutaten-tab-pane" role="tabpanel" aria-labelledby="zutaten-tab" tabindex="0">
                    <!-- Zutaten START -->
                    {% for nextstep in site.data.chili-con-carne-fix.zutaten %}
                    <div class="form-check">
                        <input class="form-check-input" type="checkbox" value="" id="flexCheckDefault" />
                        <label class="form-check-label" for="flexCheckDefault">
                            {{ nextstep.s }}
                        </label>
                    </div>
                    {% endfor %}
                    <!-- Zutaten ENDE -->
                </div>
                <div class="tab-pane fade" id="zubereitung-tab-pane" role="tabpanel" aria-labelledby="zubereitung-tab" tabindex="0">
                    <!-- Zubereitung START -->
                    {% if page.zeitaufwandzubereitung %}
                        <h5><b><i class="fa-solid fa-hourglass-end"></i> Zubereitungszeit: <span class="badge bg-primary">{{ page.zeitaufwandzubereitung }}</span></b></h5>
                    {% endif %}
                    {% for nextstep in site.data.chili-con-carne-fix.zubereitung %}
                    <div class="form-check">
                        <input class="form-check-input" type="checkbox" value="" id="flexCheckDefault" />
                        <label class="form-check-label" for="flexCheckDefault">
                            {{ nextstep.s }}
                        </label>
                    </div>
                    {% endfor %}
                    <!-- Zubereitung ENDE -->
                </div>
            </div>
        </div>
    </div>
</section>