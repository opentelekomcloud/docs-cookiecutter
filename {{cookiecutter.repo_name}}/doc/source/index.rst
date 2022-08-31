{%- macro set_header_markup(header_text_length) -%}
{%- set module_name_length = cookiecutter.repo_name|length -%}
{%- for _ in range(0, module_name_length + header_text_length) -%}={%- endfor -%}
{%- endmacro -%}
{%- macro set_header(header_text) -%}
{{ set_header_markup(header_text|length) }}
{{header_text}}{{cookiecutter.repo_name}}
{{ set_header_markup(header_text|length) }}
{%- endmacro -%}

{{ set_header("Welcome to the documentation of ") }}
