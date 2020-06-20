The documentation is here:

[macros](https://mkdocs-macros-plugin.readthedocs.io/en/latest/)

## Variables

The price of the product is {{ price }}.

See [more information on the website]({{ company.website }}).

See <a href="{{ company.website }}">more information on the website</a>.

## Input fields with macro

{% macro input(name, value='', type='text', size=20) -%}
    <input type="{{ type }}" name="{{ name }}" value="{{
        value|e }}" size="{{ size }}">
{%- endmacro %}

<p>Username: {{ input('username') }}</p>
<p>Password: {{ input('password', type='password') }}</p>


## Git information

{{ git.short_commit}} ({{ git.date}}) by {{ git.author}}

{{ context(git)| pretty }}

## Include

{% include 'docs/snippet.md' %}

The attempt to include different file

```yaml
{% include 'mkdocs.yml' %}
```