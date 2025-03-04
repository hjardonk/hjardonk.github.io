---
layout: default
title: Publications
---

<h1>Publications</h1>
<ul id="publications-list">
  <!-- The list will be populated by JavaScript -->
</ul>

<script>
  document.addEventListener("DOMContentLoaded", function () {
    const arxivIDs = [
      "2502.08276",
      "2408.00487"
    ];

    const listElement = document.getElementById("publications-list");

    arxivIDs.forEach(id => {
      fetch(`https://export.arxiv.org/api/query?id_list=${id}`)
        .then(response => response.text())
        .then(str => (new window.DOMParser()).parseFromString(str, "text/xml"))
        .then(data => {
          const entry = data.querySelector("entry");
          if (!entry) return;

          const title = entry.querySelector("title").textContent.trim();
          const summary = entry.querySelector("summary").textContent.trim();
          const link = entry.querySelector("id").textContent.trim();

          const li = document.createElement("li");
          li.innerHTML = `
            <strong><a href="${link}" target="_blank">${title}</a></strong>
            <button onclick="this.nextElementSibling.classList.toggle('hidden')">Abstract</button>
            <p class="hidden">${summary}</p>
          `;

          listElement.appendChild(li);
        })
        .catch(error => console.error("Error fetching arXiv data:", error));
    });
  });
</script>

<style>
  .hidden {
    display: none;
  }
</style>
