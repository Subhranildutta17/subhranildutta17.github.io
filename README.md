# subhranildutta17.github.io

Personal academic website of Subhranil Dutta, built with [Jekyll](https://jekyllrb.com/) and published by GitHub Pages.

## Where to edit things

You should rarely need to touch HTML. Almost everything is plain text in these files:

| What you want to change | File |
|---|---|
| Name, position, affiliation, photo, email, research interests, Scholar/DBLP/CV links, contact details | `_config.yml` |
| "About Me" paragraphs on the home page | `index.md` |
| Latest News box | `_data/news.yml` |
| Publications (conference and journal) | `_data/publications.yml` |
| Talks | `_data/talks.yml` |
| Reviewing and PC service | `_data/service.yml` |
| Degrees (Academic page) | `_data/education.yml` |
| Awards page | `_data/awards.yml` |
| Teaching tables and teaching philosophy | `_data/teaching.yml` |
| Menu items | `_data/navigation.yml` |
| Colours and fonts | `assets/css/main.scss` (the `:root` block at the top) |

After you commit a change on GitHub, the live site updates in about a minute.

### Example: adding a paper

Open `_data/publications.yml`, copy an existing block and edit it. Put the newest paper at the top. List all authors in the order printed on the paper; your own name is shown in bold automatically.

```yaml
  - title: "Your New Paper Title"
    authors: [Subhranil Dutta, First Coauthor, Second Coauthor]
    venue: CRYPTO 2027
    venue_long: "Advances in Cryptology – CRYPTO 2027"
    year: 2027
    doi: 10.1007/...
    eprint: 2027/123      # optional
```

### Example: adding a news item

At the top of `_data/news.yml`:

```yaml
- date: Dec 2026
  text: Paper accepted at [Eurocrypt 2027](https://eurocrypt.iacr.org/2027/).
```

YAML tips: keep the indentation exactly as in the neighbouring entries (spaces, not tabs). If a title contains a colon `:`, wrap it in double quotes.

## Publishing (first time)

1. Upload everything in this folder to the root of the `subhranildutta17.github.io` repository (GitHub: **Add file > Upload files**, drag the folder contents in, commit). Make sure the `_config.yml`, `_data`, `_includes`, `_layouts` and `_sass` folders are included.
2. Delete the old files that are no longer used: `styles.css`, `IMG_1160.jpg`, `IMG_1317.jpg`, `your-picture.jpg`. (They are already excluded from the build, but the original photos contain the phone's GPS location in their metadata.)
3. In **Settings > Pages**, the source should be "Deploy from a branch", branch `main`, folder `/ (root)`. That is GitHub's default, so nothing usually needs changing.
4. Check the **Actions** tab: a "pages build and deployment" run should go green within a minute or two.

The old address `academic_qualification.html` redirects to `academic.html`, and the Google Search Console verification file is kept.

## Previewing on your own computer (optional)

Requires Ruby 3.x.

```sh
bundle install
bundle exec jekyll serve
```

Then open <http://localhost:4000>. The `Gemfile` pins the same Jekyll version and plugins that GitHub Pages uses.
