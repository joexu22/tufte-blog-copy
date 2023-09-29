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
        - entry point for apache
        - output/post.html
    - sudo systemctl restart httpd

  - Pandoc without pkg manager, cause I accidentally am using Amazon Linux 2023 (what is this no EPEL)
    - wget https://github.com/jgm/pandoc/releases/download/3.1.8/pandoc-3.1.8-linux-amd64.tar.gz
    - tar xvzf pandoc-3.1.8-linux-amd64.tar.gz
    - sudo mv pandoc-3.1.8/bin/* /usr/local/bin/

  - Linux Notes
    - sudo apachectl configtest
    - sudo systemctl restart httpd
    - rsync -av --delete ./output/ /var/www/html/output/
