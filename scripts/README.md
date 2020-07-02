## Documenting the Provider

### Terraform Provider Schema

The docs for this provider are autogenerated from the 
`terraform providers schema -json ` command

A `docgen.py` script will convert this output into a Markdown file. The file is then split to 
`Resources` and `Datasources`. The entire output is in the index of the docs page.

### Using Github Pages Locally

Install:
* Ruby
* Bundler (via `gem`)
* Jekyll (via `gem`)

Create a Gemfile in the root of the repo with:

```
source 'https://rubygems.org'
gem "just-the-docs"
gem 'github-pages', group: :jekyll_plugins
```

Run `bundle exec jekyll serve`
