# GECO website

- Fork the repo to your own account
- open the RStudio project
- run `blogdown::serve_site()` to render the site
- add or change data in `content/` to add content
  - `post` containts blog posts
  - `home` is the main page content
  -  etc..
- the site will rerender upon changes
- stop the server using `blogdown::stop_server()`

Note: changes to the theme are not automatically updated.

To link to a bought domain set a cname parameter in the github actions
workflow at the build stage to the correct domain instead of a github location.

Change the `config/_default/*.yaml` files to change site parameters.

## Adding content 

If you don't have writing rights to the repository from which the website is created (currently `computationales/geco_website`), then fork the repository, commit and push changes (added content) to your fork and create a pull request to `computationales/geco_website`.

### Publications

Instructions are given [here](https://wowchemy.com/docs/content/publications/). 

Make sure you have the `academic` library installed.
```sh
pip3 install -U academic
```

A bibtex file is included in this repository as `data-raw/publications_geco.bib`. Add the citation information (bibtex-formatted) as text to that file. Then create a new item for the website by:
```sh
academic import --bibtex data-raw/publications_geco.bib
```

### Blog post

Instructions are given [here](https://wowchemy.com/docs/content/blog-posts/).

To create a blog/news article:
```sh
hugo new  --kind post post/my-article-name
```

Then edit the newly created file `content/post/my-article-name.md` with your full title and content.