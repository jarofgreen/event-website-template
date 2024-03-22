# Event Website Template

When someone is running a regular event, we think they should have a simple website to communicate essential information openly and publicly.

While they can also use other services to promote their events, it's good to have a presence online that they own and control.

This repository is a template for such a website.

## Features

A blog section.

An events listing section.

Static pages; starts with pages about the group and contact information.

Links section.

Basic design to customise.

[Schema.org](https://schema.org/) markup for SEO and data reuse.

[DataTig](https://github.com/DataTig) admin site, for easier site editing and data reuse. Available at /datatig in your website.

## Technical information

The website is a static website that can be entirely built and hosted on GitHub or other good hosting services with pages and build capabilities.

## How to use

Simply fork this repository, edit as needed and go!

## Develop locally

To build the Jekyll site:

```
docker run --rm   --volume="$PWD:/srv/jekyll:Z" -p 4000:4000 -it jekyll/builder:4 /bin/bash -c 'gem install webrick && jekyll serve'
```


To build the DataTig admin site:

```
pip install datatig
python -m datatig.cli build . --staticsiteoutput _site/datatig
```

## Roadmap

Future DataTig versions will allow better event editing, 
and allow creation of public ical feeds for people to import straight into calendars.

## To host on GitHub

Go to settings, pages and for the “source” option select “Github Actions”.

