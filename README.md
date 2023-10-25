# SignUp Disney+ Info

**This repository is part of a project to determine variables that could predict future Disney+ titles that will receive American Sign Language (ASL) captioning via the browser extension [SignUp](signupcaptions.com).**
However, several of its parts can be used or adapted to scrape [Flixable](flixable.com) or SignUp for info on any services they support.

## Overview

[SignUp](signupcaptions.com) is a free Chrome extension that deploys sign captioning on supported titles on streaming services. Essentially, when the extension is installed, it will automatically pull up a YouTube video of an ASL interpretation of a supported streaming title. This video can be resized and repositioned. The extension can also be clicked from a browser's toolbar to provide links to all supported titles' pages on their streaming services. Currently, SignUp supports American Sign Language, British Sign Language, and Indian Sign Language on select shows across Disney+, Disney+ Hotstar, Netflix, and Peacock.
SignUp has a form on its website to allow users to request an interpretation; my goal is simply to see what trends the supported titles on Disney+ seem to follow and which titles are most likely to receive interpretation in the future.

[Flixable](flixable.com) is a website that aggregates information on new additions to streaming services and logs which titles are available on these services. Presently Flixable has listings for Netflix, Disney+, Max, and Hulu, as well as ways to stream certain popular TV channels live.

## Current files

* **Flixable Scraping.ipynb**: a Jupyter Notebook that scrapes Flixable to get data on all titles currently available on Disney+. It first scrapes Flixable's list of all Disney+ titles, then it scrapes each title's own page on Flixable.
  * Required Python packages:
    * selenium
    * pandas
    * bs4
    * requests
    * re
    * time
* **flixable.csv**: output of the above file, containing columns for title, IMDb rating, content rating (MPAA or TV), release year, runtime (minutes or seasons), date added to Disney+, and genres, as well as links to each individual Flixable page.
