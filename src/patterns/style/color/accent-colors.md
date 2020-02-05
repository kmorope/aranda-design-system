---
title: Feedback
styles: base/variables.scss
maturity: draft
control: exclude
colors:
  - name: $green1
    hex: '#009145'
    rgb: rgb(0,145,69)
  - name: $green2
    hex: '#a1bc00'
    rgb: rgb(161,188,0)
  - name: $orange
    hex: '#ffa300'
    rgb: rgb(255,163,0)
  - name: $yellow
    hex: '#ffcc00'
    rgb: rgb(255,204,0)
  - name: $red
    hex: '#ff0000'
    rgb: rgb(255,0,0)
  - name: $purple
    hex: '#8962b2'
    rgb: rgb(137, 98,178)
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
