# Twig

## Metadata Rendering

Avoid manually looping through `page.metadata` as a simple key/value array.

Incorrect:

```twig
{% for name, content in page.metadata %}
<meta name="{{ name }}" content="{{ content }}">
{% endfor %}
```

Correct:

```twig
{% include 'partials/metadata.html.twig' %}
```

This follows Grav 1.7 conventions and avoids Array to string conversion errors.
