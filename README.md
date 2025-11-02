# Nelson Tech Meetup Website

A static website for the Nelson Tech Meetup community, built with [Hugo](https://gohugo.io/) and [Bootstrap 5](https://getbootstrap.com/), and automatically deployed to GitHub Pages.

## Creating Meeting Content

Meeting content is stored in the `content/meetings/` directory as Markdown files. Each meeting is a separate file named with the meeting date in `YYYY-MM-DD.md` format.

Each meeting file starts with YAML front matter that defines the meeting metadata:

```yaml
---
title: "Meeting Title"
date: 2025-11-26T18:00:00-08:00   # Meeting date/time (ISO 8601 format)
time: "6:00 PM - 8:00 PM"         # Display time (optional)
category: tech                    # Category: ai, tech, or social
location:
  name: Nelson Innovation Centre
  address: 91-d Baker St, Nelson, BC V1L 4G8
  instructions: "Optional instructions for finding the venue"
speakers:
  - name: "Speaker Name"
    bio: "Speaker biography"
    website: "https://speaker-website.com"  # Optional
resources:
  - title: "Event Details (Facebook)"
    url: "https://facebook.com/events/..."
  - title: "Slides"
    url: "https://example.com/slides.pdf"
---
```

## Development

Contributions are welcome! Please make contributions in the form of a well described [Pull Request](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/about-pull-requests).

For simple content changes, consider using the "Edit this page on GitHub" link on any page to suggest changes directly.

Running locally requires [Hugo Extended](https://gohugo.io/installation/) (v0.152.2 or later) to be installed.

## Deployment

The site is automatically built and deployed to GitHub Pages using GitHub Actions. The workflow is triggered by:

- **Push to `main` branch**: Immediately builds and deploys the site
- **Manual trigger**: Via the Actions tab in GitHub
- **Daily schedule**: Rebuilds every day at midnight Pacific Time (8 AM UTC) to keep the "upcoming" vs "past" meetings current