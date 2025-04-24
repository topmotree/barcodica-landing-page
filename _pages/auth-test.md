---
layout: page
title: Auth Test
include_in_header: false
robots: noindex
---

# Auth Test

This page is used to test OAuth authorization. Click the button below to proceed.

<button id="redirect-button">Open in App</button>

<script>
  document.getElementById('redirect-button').addEventListener('click', function () {
    // Get the current URL's query parameters
    const queryParams = new URLSearchParams(window.location.search);

    // Construct the custom URL scheme
    const customUrl = `myapp://?${queryParams.toString()}`;

    // Redirect the user to the custom URL
    window.location.href = customUrl;
  });
</script>