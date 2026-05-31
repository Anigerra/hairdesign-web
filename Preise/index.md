---
layout: default
title: Preise

---

<div class="container">
    <div class="block">
        <h1 class="title has-text-centered">Leistungen und Preise</h1>
    </div>
    {% for sec in site.data.preise.sections %}
    <div class="block">
        <div class="columns">
        <div class="column mx-4">
            <div class="columns is-mobile mb-0">
                <div class="column is-half mgl-small">
                <p class="has-text-weight-bold">
                    {{ sec.name | upcase }}
                </p>
                </div>
                <div class="column">
                    <p>Irina</p>
                </div>
                <div class="column">
                    <p>Ioanna</p>
                </div>
            </div>
            <hr class="mt-0"/>
            {% for subsec in sec.subsections %}
            <p class="{{subsec.class}} pb-2">{{ subsec.name | upcase }}</p>
                {% for leistung in subsec.leistungen %}
                    <div class="columns is-mobile">
                        <div class="column is-half mgl-small">
                            <p>{{ leistung.name | upcase }}</p>
                            <p class="has-text-weight-light">{{ leistung.genauer }}</p>
                        </div>
                        <div class="column">
                            <p>{{ leistung.preis }}</p>
                        </div>
                        <div class="column">
                            <p>{{ leistung.top }}</p>
                        </div>
                    {% endfor %}
                {% endfor %}
            </div>
            </div>
        </div><!-- end block -->
    {% endfor %}
    <div class="block">
    <p class="footer has-text-weight-light">
        * Auszug aus unserer Preisliste in Euro. Die angegebenen Preise sind Grundpreise, die von einem durchschnittlichen Aufwand ausgehen. Bei höherem Aufwand erhalten Sie ein separates Angebot. Bezahlung in Bar oder via EC-Karte möglich. 
    </p>
    </div>
</div><!-- end container -->
