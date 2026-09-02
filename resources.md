---
title: "Needham Circle — Community Resources"
description: "Community resources for Needham: town offices, affinity groups, nonprofits, and parks."
permalink: /resources
wide: true
---

<h2>Community Resources</h2>

{% for section in site.data.resources %}
  <section class="resource-section">
    <h3>{{ section.title }}</h3>
    <table class="resource-table">
      <thead>
        <tr>
          <th scope="col">Organization</th>
          <th scope="col">Description</th>
          <th scope="col">Website</th>
        </tr>
      </thead>
      <tbody>
        {% for entry in section.entries %}
          <tr>
            <th scope="row">{{ entry.name }}</th>
            <td data-label="Description">{{ entry.desc }}</td>
            <td data-label="Website">
              {% if entry.href %}
                <a href="{{ entry.href }}" title="{{ entry.cont }}" target="_blank" rel="noopener noreferrer"><span class="contact-label">Website</span><span class="contact-value">{{ entry.cont }}</span></a>
              {% else %}
                {{ entry.cont }}
              {% endif %}
            </td>
          </tr>
        {% endfor %}
      </tbody>
    </table>
  </section>
{% endfor %}
