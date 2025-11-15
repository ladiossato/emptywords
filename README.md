# Empty Words

Clean, modern, minimalist website for Empty Words writings.

## Adding New Writings

Create a new markdown file in `_writings/` folder:

**Filename format:** `YYYY-MM-DD-title-slug.md`

**Example:** `2024-11-15-your-writing-title.md`

**Front matter:**
```markdown
---
title: "Your Writing Title"
date: 2024-11-15
---

Your writing content here...
```

**Push to GitHub:**
```bash
git add _writings/2024-11-15-your-writing.md
git commit -m "Add new writing"
git push
```

Site updates automatically in 1-2 minutes.

## File Structure

```
emptywords/
├── _config.yml          # Site configuration
├── _layouts/            # Page templates
├── _includes/           # Reusable components  
├── _writings/           # ✨ Your writings go here
├── assets/css/          # Styling
├── index.md            # Home page
├── about.md            # About page
└── writings.md         # Writings archive
```

## Local Development (Optional)

```bash
# Install Jekyll
gem install bundler jekyll

# Install dependencies
bundle install

# Run local server
bundle exec jekyll serve

# View at: http://localhost:4000
```

## Deployment

### GitHub Pages Setup

1. Push to GitHub
2. Settings → Pages → Deploy from branch: main, / (root)
3. Site live at: `https://ladiossato.github.io/emptywords`

### Custom Domain (empty-words.com)

**In Squarespace DNS:**
- A Record: @ → 185.199.108.153
- A Record: @ → 185.199.109.153
- A Record: @ → 185.199.110.153
- A Record: @ → 185.199.111.153
- CNAME: www → ladiossato.github.io

**In GitHub:**
- Settings → Pages → Custom domain: `empty-words.com`
- Enable "Enforce HTTPS" (after DNS propagates)

**In _config.yml:**
```yaml
baseurl: ""  # Set to "" once custom domain is active
```

## Design Philosophy

- **Clean & Modern:** Inspired by tr.af aesthetic
- **Crisp Typography:** Modern sans-serif, refined spacing
- **Generous White Space:** Breathing room for contemplative content
- **Highly Refined:** Professional, polished, intentional
- **Responsive:** Beautiful on all devices
- **Dark Mode:** Automatic based on system preference

## Your Workflow

```
1. Write: Create .md file in _writings/
2. Commit: Push to GitHub
3. Wait: 90 seconds
4. Live: Published on empty-words.com
```

That's it.

## Contact

Email: ladiossato@gmail.com  
Subscribe: https://ladiossato.short.gy/subscribe
