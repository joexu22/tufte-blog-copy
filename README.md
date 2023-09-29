# Overview
Getting this to build & run on website

# Old Content
Tufte-Blog is the system I use for composing blog posts. Posts are written in Markdown format,
converted to HTML using [Pandoc][pandoc], and postprocessed by [`build.py`](build.py), which
generates the final output. The HTML files are styled using [Tufte CSS][tufte_css].

See the example site [here.][site]

[tufte_css]: http://github.com/edwardtufte/tufte-css
[pandoc]: http://pandoc.org
[site]: http://adityaramesh.com/tufte-blog/posts.html

# Notes

## EC2 Deployments
  - Apache
    - etc/httpd/conf/httpd.conf
        - entry point for apachett
    - sudo systemctl restart httpd