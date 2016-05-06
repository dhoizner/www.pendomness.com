---
layout: page
title: Pen Collection
permalink: /pens/
---

{% include data_tables.html %}

<script>
  $(document).ready( function () {
    $('#pens').DataTable( {
      paging: false
      } );
    });
</script>

<table id="pens" class="display compact" cellspacing="0" width="100%">
  <thead>
    <tr>
      <th>Brand</th>
      <th>Model</th>
      <th>Sub-Model</th>
      <th>Color</th>
      <th>Nib(s)</th>
      <th>Type</th>
      <th>Country</th>
      <th>Sell?</th>
    </tr>
  </thead>
  <tbody>
    {% for pen in site.data.pens %}
      <tr>
        <td>{{ pen.Brand }}</td>
        <td>{{ pen.Model }}</td>
        <td>{{ pen.Sub-Model }}</td>
        <td>{{ pen.Color }}</td>
        <td>{{ pen.Nibs }}</td>
        <td>{{ pen.Type }}</td>
        <td>{{ pen.Country }}</td>
        <td>{{ pen.Sell? }}</td>
      </tr>
    {% endfor %}
  </tbody>
</table>
