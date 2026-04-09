# Italian Booklets

These booklets are a simple and practical tool, intended for use both independently and
during Italian courses for foreigners. They were created in Trieste by some
friends of Piazza del Mondo (piazza Libertà) and can be found in the Italian
language schools for foreigners in the city.

## About the website

This website relies on [Jekyll](https://jekyllrb.com/) for layouts and template
features, and is built and served by [GitHub Pages](https://docs.github.com/en/pages).

To edit this website locally on your computer and see results in real-time, you
need to install Jekyll. And since this website is just a Git repository hosted
by GitHub Pages, it will be convenient to install [Git](https://git-scm.com/).
See the first few pages of [Pro Git](https://git-scm.com/book/) by Scott
Chacon and Ben Straub for a quick introduction to the Git version control
system.

Setting up Jekyll involves

- installing Ruby, RubyGems, GCC and Make,
- configuring RubyGems installation directory (a user directory is
  recommended),
- installing Jekyll and Bundler as Gems.

Refer to Jekyll Docs for detailed and up to date [installation
instructions](https://jekyllrb.com/docs/installation/) for different operating
systems.

With Jekyll and Git installed you are ready to make edits to the website. Start
by cloning the Git repository.

```
$ git clone https://github.com/italianbooklets/italianbooklets.github.io
```

Change into the cloned directory.
```
$ cd italianbooklets.github.io
```

Build the site and serve it locally on [http://localhost:4000](http://localhost:4000).
```
$ bundle exec jekyll serve
```

Any changes to source files will prompt a rebuild, and you can see the new
version by refreshing the page.

## Adding a new booklet

Booklet PDFs are contained in the directory `assets/booklets/`. Other
information about booklets is contained in the file `_data/languages.yml`. For
example, the Nepalese booklet is saved as `Italian___English___Nepali.pdf` in
the `assets/booklets/` directory, and its corresponding section in
`languages.yml` is as follows.
```yml
- lang: Nepalese
  booklet: 'Italian___English___Nepali.pdf'
```

To add a new booklet, copy its PDF file to `assets/booklets/` and add a section
to the `_data/languages.yml` file whose `lang` field is set to the new language
and `booklet` field is set to the file name of the PDF. When the website is
rebuilt, a new section will automatically be added to the main page.

## Updating an existing booklet

Updating an existing booklet can be as simple as replacing the old PDF file
with a new one which has the same name as before. If the new file has a
different name (indicating version number, perhaps), then its `booklet` entry in
`_data/languages.yml` should also be updated to the new file name (see above).

