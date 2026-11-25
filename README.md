# MET provenance gaps and actors of African Art Objects

The Metropolitian Museum of Art is an encylopedic collection of art and artifacts from a variety of cultures that span centuries. However, the origins of many of these objects specifically within the African art collection has significant gaps and uncertainties within the provenance records. I chose to investigate these gaps and the actors associated with African cultural objects created between the 19th and 20th centuries.

## Process Disclaimers

I had originally planned to utilize the MET's API which has 56 columns of information, however, notably lacks provenance as a category. To troubleshoot this issue, I applied webscraping individual pages in order to obtain provenance records from JSON embedded into HTML. Due to the lack of automation available for the webscraping, I had collected a sample of 210 records between the 19th and 20th centuries on the default 'relavance' sort through their web facing collection search. Further research could include a larger sample since 2,815 objects are within the time frame of creation and from Africa.

The MET API groups objects by Department and notably the African Art falls under the Michael C. Rockefeller Wing which includes Africa, Oceania, and the Americas. This is notably the only category named after a wing rather than the region and is also difficult to then locate items as a filter would need to include 56 countries within the continent. 


## Context and Methodology

This home page links to two other Markdown files in the repo. Click them to see linking in action:

- [Objects Investigated](about.md) — an example page with embedded tables and images
- [Backend Methodology](embedding-code.md) — an example page with code examples (both as static markdown and as interactive [pyodide](https://pyodide.org/en/stable/) snippets)
- [A JupyterLite notebook](notebook/notebooks/index.html?path=week10.ipynb) hosted on your GitHub pages site, which can run in the browser without your viewers needing to have Jupyter Lab/Anaconda etc installed


## How It Works

- GitHub Pages runs a tool called [Jekyll](https://jekyllrb.com/) on your repo automatically every time you push. It converts each `.md` file into an `.html` page.
- **`README.md` is the home page.** If there's no `index.md` in the repo, GitHub Pages uses `README.md` as the landing page.
- **Linking between pages is just a normal Markdown link.** Write `[About the Project](about.md)` and GitHub Pages rewrites it to `about.html` when it builds the site. Because the link points to the `.md` file, it also works when browsing the repo on GitHub.com.
- **No front matter required.** You don't need the `---` block some Jekyll tutorials show at the top of each file. Each page's first `# Heading` is used as its title.
- **`_config.yml` controls site-wide settings.** In this repo it only sets the site title, description, and theme. Try changing the `theme:` line to another [supported theme](https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/adding-a-theme-to-your-github-pages-site-using-jekyll/) such as `jekyll-theme-cayman`.

## Publishing Your Site on GitHub.com

1. **Make your own copy.** [Navigate to this repo on github.com.](https://github.com/craigfahner/664-pages-template). Click **Use this template → Create a new repository** at the top of this repo on GitHub.com (or fork it). Give the repository a name; it will become part of your site's URL.
![template](template.png)
2. **Turn on GitHub Pages.** In your new repo, go to **Settings → Pages**. Under **Build and deployment**, set **Source** to **GitHub Actions**. (The workflow in `.github/workflows/pages.yml` builds the site, including the JupyterLite notebook. If its first run failed because Pages wasn't turned on yet, open the **Actions** tab and re-run it.)
3. **Wait for the build.** Open the **Actions** tab to watch the "Build and deploy site" workflow. It usually takes a few minutes.
4. **Visit your site.** It will be at:

   ```
   https://YOUR-USERNAME.github.io/YOUR-REPO-NAME/
   ```

   The link also appears at the top of **Settings → Pages** once the site is live.
5. **Edit and push.** Any change pushed to `main`, including edits made directly on GitHub.com with the pencil icon, rebuilds the site automatically.

## Adding a New Page

1. Create a new file ending in `.md`, for example `gallery.md`.
2. Start it with a heading: `# Gallery`.
3. Link to it from this README: `[Gallery](gallery.md)`.
4. Commit and push. The new page appears on the site after the next build.

## Troubleshooting

- **404 on the site?** Make sure Pages is enabled (step 2 above) and the build in the **Actions** tab finished with a green check.
- **A link is broken?** Check the filename's spelling and capitalization. `About.md` and `about.md` are different files.
- **Changes aren't showing?** Wait for the build to finish, then hard-refresh your browser (Shift + Reload).
