# wiki
Monk OS Wiki

Steps to Push pages

1. mkdir docs && cd docs
2. mkdir wiki-gen
3. git clone https://github.com/emonkos/wiki.git
4. git clone https://github.com/emonkos/wiki.git wiki-gen/html
5. cd wiki
6. make your changes changes
7. compile using `make html`
8. commit in master branch
9. cd ../wiki-gen/html/
10. commit your changes in gh-pages
11. push both repos

Reference: https://daler.github.io/sphinxdoc-test/includeme.html
