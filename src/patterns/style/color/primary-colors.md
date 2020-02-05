---
title: Neutral Colors
styles: base/variables.scss
maturity: ready
control: exclude
colors:

  - name: $grey1
    hex: '#666666'
    rgb: rgb(102,102,102)
  - name: $grey2
    hex: '#999999'
    rgb: rgb(153,153,153)
  - name: $grey3
    hex: '#b8b8b8'
    rgb: rgb(184,184,184)
  - name: $grey4
    hex: '#CCCCCC'
    rgb: rgb(204,204,204)
  - name: $grey5
    hex: '#DDDDDD'
    rgb: rgb(221,221,221)
  - name: $grey6
    hex: '#E0E0E0'
    rgb: rgb(224,224,224)
  - name: $grey7
    hex: '#EAEAEA'
    rgb: rgb(234,234,234)
  - name: $grey8
    hex: '#EFEFEF'
    rgb: rgb(239,239,239)
  - name: $grey9
    hex: '#F1F1F1'
    rgb: rgb(241,241,241)
  - name: $white
    hex: '#FFFFFF'
    rgb: rgb(255,255,255)

---
<style>
.set {
  display: flex;
  flex-wrap: wrap;
  margin: 0 -1rem;
  margin-top: 0;
  padding: 0;
  list-style: none;
}
li {
  flex: 1 0 20%;
  margin: 1rem;
}
.color {
  width: 100%;
  min-width: 160px;
  height: 80px;
  color: white;
  border: 1px solid whitesmoke;
  margin-bottom: 1rem;
}
p {
  margin: 0;
}
</style>
<ul class="set">
{% for item in page.colors %}
  <li>
    <div class="color" style="background:{{ item.hex }}"></div>
    <p>{{ item.name }}</p>
    {% if item.hex %}<p>{{ item.hex }}</p>{% endif %}
    {% if item.rgb %}<p>{{ item.rgb }}</p>{% endif %}
  </li>
{% endfor %}
</ul>
