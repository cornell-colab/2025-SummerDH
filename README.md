# Roadmap for this Site
This site is a really basic Jekyll-powered static site, with a few JavaScript plugins for search and better content arrangement.

## Folder Structure
- `_data`: includes a bunch of structure yml files, including the navigation file. If you need to change anything in the navbars, edit the `navigation.yml file.`
- `_drafts`: storage folder for alternative page layouts, if needed.
- `_includes`: holds all of the Jekyll includes (functional internal plugins, basically) for the site. **Exercise aution when editing.**
- `_layouts`: includes the page layouts/templates. **Exercise aution when editing.**
- `_sass`: includes the individual stylesheets for the site, which are imported into the main css file in the assets folder. If you want to change the styling of something, change it in these files, not the main CSS file. **Exercise aution when editing.**
- `_assets`: contains the main CSS and JavaScript for the site. **Exercise aution when editing.**
- `images`: contains all images embedded in the site (the logo, card fronts, etc.)
- `pages`: includes all content for the site, organized into subfolders by the date of the lesson.

The `Gemfile` and `Gemfile.lock` folders are what set the Ruby version and dependencies for Jekyll. The `_config.yml1 file uncludes the general configuration settings for the site.

## Editing
- To edit content on a single page or to create a new page, edit/create Markdown files in the dated subfolder for your lesson within the `pages` folder. For example, to edit the Web Programming lesson on June 4th, I would go to: `pages > June 4 > COLLX: Web Programming.md` and edit that file.
  - Every page **must** have Jekyll front matter with a permalink, title, layout, etc. Please see the existing pages in the `pages` folder for what needs to be in the front matter and how to format it.
- The front page of the site is located at: `pages > pages-root-folder > index.md`.
- There are individual pages with the calendar and assignment lists for each cohort at `pages > collections.md` and `pages > text.md`. Feel free to edit these as you wish. They're currently connected to the COLLECTIONS and TEXT nav items. 
- To edit the navigation, go to `data > navigation.yml`. Note that the URL you set for a page in the navigation must match the URL you set in the Jekyll front matter for that same page.
  - The permalink for a lesson that goes in the ALL category will start with `/modules`. For TEXT, it will be `text`. For COLLX, it will be `collections`.

## Questions
Uh just email me or Slack me and I'll fix whatever's broken! Or walk you through something! Hooray for co-learning!
