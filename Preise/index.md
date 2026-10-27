---
layout: default
title: Preise

---

<div class="container">
    <div class="block">
        <h1 class="title has-text-centered">Leistungen und Preise</h1>
    </div>
    {% for sec in site.data.preise.sections %}
        <div class="block is-centered">
            <div class="columns">
            <div class="column mx-4">
                <div class="columns mb-0">
                    <div class="column is-three-fifths is-offset-one-fifth is-two-third-mobile mgl-small">
                    <p class="has-text-weight-bold">
                        {{ sec.name | upcase }}
                    </p>
                    </div>
                </div>
                <div class="columns my-0">
                    <div class="column is-three-fifths is-offset-one-fifth">
                        <hr class="my-0"/>
                    </div>
                </div>
                {% for subsec in sec.subsections %}
                    <div class="columns my-0">
                        <div class="column is-three-fifths is-offset-one-fifth mgl-small">
                            <p class="{{subsec.class}} pb-2">{{ subsec.name | upcase }}</p>
                        </div>
                    </div>
                    {% for leistung in subsec.leistungen %}
                        <div class="columns is-mobile">
                            <div class="column has-text-centered mgl-small "></div>
                            <div class="column is-two-fifths is-half-mobile mgl-small">
                                <p>{{ leistung.name | upcase }}</p>
                                <p class="has-text-weight-light">{{ leistung.genauer }}</p>
                            </div>
                            <div class="column has-text-centered is-one-third-mobile mgl-small ">
                                <p>{{ leistung.preis }}</p>
                            </div>
                            <div class="column has-text-centered mgl-small "></div>
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
