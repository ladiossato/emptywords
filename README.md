# Empty Words

Minimalist website for Empty Words writings.

## How to Add a New Writing

1. Create a new markdown file in `_writings/` folder
2. Name it: `YYYY-MM-DD-title-slug.md`
3. Add front matter at the top:

```markdown
---
title: "Your Writing Title"
date: 2024-11-15
---

Your writing content here...
```

4. Commit and push to GitHub:

```bash
git add _writings/2024-11-15-your-writing.md
git commit -m "Add new writing: Your Title"
git push
```

5. Wait 1-2 minutes for GitHub Pages to rebuild
6. Your writing will appear automatically on the site

## Front Matter Options

Minimal front matter needed:

```yaml
---
title: "Writing Title"
date: 2024-11-15
---
```

Optional fields:

```yaml
---
title: "Writing Title"
date: 2024-11-15
excerpt: "Custom preview text (otherwise uses first paragraph)"
---
```

## Local Development (Optional)

If you want to preview locally before pushing:

1. Install Jekyll:
```bash
gem install bundler jekyll
```

2. Create a Gemfile in the root:
```ruby
source "https://rubygems.org"
gem "jekyll", "~> 4.3"
gem "webrick", "~> 1.8"
```

3. Install dependencies:
```bash
bundle install
```

4. Run local server:
```bash
bundle exec jekyll serve
```

5. View at: `http://localhost:4000`

## Deployment to GitHub Pages

### Initial Setup

1. Push all files to your GitHub repository
2. Go to repository Settings → Pages
3. Under "Source", select "Deploy from a branch"
4. Under "Branch", select "main" and "/ (root)"
5. Click Save
6. Your site will be live at `https://[username].github.io/[repo-name]`

### Connect Custom Domain (Squarespace DNS)

1. In your repository, create a file called `CNAME` in the root:
```
emptywords.com
```

2. In Squarespace DNS settings, add these records:
   - Type: `A` → Host: `@` → Points to: `185.199.108.153`
   - Type: `A` → Host: `@` → Points to: `185.199.109.153`
   - Type: `A` → Host: `@` → Points to: `185.199.110.153`
   - Type: `A` → Host: `@` → Points to: `185.199.111.153`
   - Type: `CNAME` → Host: `www` → Points to: `[username].github.io`

3. In GitHub repository Settings → Pages:
   - Enter your custom domain: `emptywords.com`
   - Enable "Enforce HTTPS" (may take a few hours)

4. Wait 24-48 hours for DNS propagation

## Site Structure

```
emptywords/
├── _config.yml          # Site settings
├── _layouts/            # Page templates
├── _includes/           # Reusable components
├── _writings/           # ✨ Your writing files go here
├── assets/css/          # Styling
├── index.md            # Home page
├── about.md            # About page
└── writings.md         # Writings archive
```

## Writing Workflow

```bash
# 1. Write your piece in a text editor
# 2. Save to _writings/YYYY-MM-DD-title.md
# 3. Push to GitHub
git add _writings/
git commit -m "New writing"
git push

# Done! Live in 1-2 minutes.
```

## Troubleshooting

**Writing not appearing?**
- Check filename format: `YYYY-MM-DD-title.md`
- Verify front matter has `title` and `date`
- Check for YAML syntax errors in front matter

**Site not building?**
- Go to repository → Actions tab
- Check build logs for errors
- Most common: invalid YAML in front matter

**Custom domain not working?**
- Verify CNAME file exists in root
- Check DNS records are correct
- Wait 24-48 hours for propagation
- Check GitHub Pages settings show your domain

## Design Philosophy

- Minimal: Only essential elements
- Readable: Optimized typography and spacing
- Contemplative: Generous whitespace
- Responsive: Beautiful on all devices
- Dark mode: Automatic based on system preference

## Contact

Email: ladiossato@gmail.com
Subscribe: https://ladiossato.short.gy/subscribe
