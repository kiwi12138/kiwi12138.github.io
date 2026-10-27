<h1 id="publications"></h1>

<h2 style="margin: 30px -10px -15px;">Publications <span style="font-size:15px;">[<a href="https://scholar.google.com/citations?user=E-Mcb5AAAAAJ&hl=en&oi=ao" target="_blank" rel="noopener">Google Scholar</a>]</span></h2>


<div class="publications">
<p style="font-size:14px;">* Equal contribution.</p>
<ol class="bibliography">
{% assign gsDataBaseUrl = 'https://raw.githubusercontent.com/song-chen1/song-chen1.github.io/' %}
{% assign url = gsDataBaseUrl | append: 'google-scholar-stats/gs_data.json' %}
{% for link in site.data.publications.main %}


<li>
<div class="pub-row">
  <div class="col-sm-3 abbr" style="position: relative;padding-right: 15px;padding-left: 15px;">
    <img src="{{ link.image }}" alt="Overview of {{ link.title | escape }}" loading="lazy" class="teaser img-fluid z-depth-1" style="object-fit: {{ link.image_fit | default: 'cover' }};">
            <abbr class="badge">{{ link.conference_short }}</abbr>
  </div>
  <div class="col-sm-9" style="position: relative;padding-right: 15px;padding-left: 20px;">
      <div class="title"><a href="{{ link.pdf }}">{{ link.title }}</a></div>
      <div class="author">{{ link.authors }}</div>
      <div class="periodical"><em>{{ link.conference }}</em>
      </div>
    <div class="links">
      {% if link.pdf %} 
      <a href="{{ link.pdf }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">PDF</a>
      {% endif %}
      {% if link.code %} 
      <a href="{{ link.code }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Code</a>
      {% endif %}
      {% if link.page %} 
      <a href="{{ link.page }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Project Page</a>
      {% endif %}
      {% if link.bibtex %} 
      <a href="{{ link.bibtex }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">BibTex</a>
      {% endif %}
      {% if link.notes %} 
      <strong> <i style="color:#e74d3c">{{ link.notes }}</i></strong>
      {% endif %}
      {% if link.others %} 
      {{ link.others }}
      {% endif %}
      {% if link.citation %} 
      <strong> <a style="color:#e74d3c; font-weight:600"> • <i class="total_citation_mtl" data-citation="{{ link.citation }}"></i> <i style="color:#e74d3c; font-weight:600"> Citations </i></a></strong>
      <script>
        $(document).ready(function () {
            var gsDataBaseUrl = 'https://raw.githubusercontent.com/song-chen1/song-chen1.github.io/';
            $.getJSON(gsDataBaseUrl + "google-scholar-stats/gs_data.json", function (data) {
                var citationEles = document.getElementsByClassName('total_citation_mtl');
                Array.prototype.forEach.call(citationEles, function(element) {
                    var citationKey = element.getAttribute('data-citation');
                    if (data['publications'][citationKey]) {
                        var numCitations = data['publications'][citationKey]['num_citations'];
                        element.innerHTML = numCitations;
                    } else {
                        element.innerHTML = 'N/A';
                    }
                });
            });
        });
      </script>
      {% endif %}
    </div>
  </div>
</div>

<br>
</li>

{% endfor %}
</ol>
</div>
