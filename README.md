# Mambu Momoh website

This folder is the source of the website. GitHub Pages builds it automatically each time something changes.

## Editing without code

1. Go to https://app.pagescms.org and sign in with GitHub.
2. Open this repository.
3. Pick a section on the left (Field journal, Publications, Collaborators and so on), edit the form, and press Save.
4. The live site updates about a minute later.

## What lives where

- `_data/*.yml`: the text you edit (the form editor writes these files).
- `index.html`: the page design. Edit only if you know HTML.
- `404.html`: the page shown for a wrong address.
- `assets/img`: photos, and `share.jpg`, the picture LinkedIn and other sites show when the link is posted.
- `assets/cv`: the CV files people download.

## The parts that update by themselves

- **Meeting notice.** `_data/event.yml` holds the ASTMH details. The bar at the top and the strip under your name change their wording by the clock (before, on the morning, while you are presenting, afterwards) and disappear after the `hide_after` date. For the next meeting, change the details and dates in that one file.
- **Citation figures and newest papers.** Read from OpenAlex (openalex.org) using your ORCID each time someone opens the site. This feeds the line under the research record, the colour of the wells on the plate, and the "Most recent" list.
- **Outbreak notices.** Read from WHO Disease Outbreak News, filtered to Ebola, Marburg and Lassa fever.

If OpenAlex or WHO cannot be reached, the site shows the figures saved in `_data/live.yml` with their date. Either feed can be switched off there (`show_openalex`, `show_who`).

## The plate

Each paper in `_data/publications.yml` fills one well, in list order, down the columns from A1. Add a paper to the list and it takes the next well. The plate holds 96.

## Before you switch on the Questions section

The answers in `_data/questions.yml` are drafts. Read and approve every answer, then set "Show this section on the website" to on.
