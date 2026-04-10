# Kaspi Law — Design Rules & Guidelines

## Stack
- Single HTML file (`index.html`) + Tailwind CSS CDN + Lucide icons CDN
- Decap CMS for blog (`admin/`)
- Deployed on Netlify + GitHub

---

## Design Rules

### DO:
- Minimal, elegant, prestigious law firm aesthetic — inspired by agmon-law.co.il
- Dark/deep palette: near-black (`#111`) background for hero + dark sections
- Alternating sections: dark (`#111`) and light off-white (`#faf8f5`)
- Accent color: warm gold/champagne (`#c9a96e`) — used sparingly on lines, borders, hover states, labels
- Typography: Frank Ruhl Libre (Google Fonts) for headings, Inter for body text
- Full RTL (`dir="rtl"` on `<html>`, `text-align: right` throughout)
- Plenty of whitespace, generous section padding (`py-24` minimum)
- Scroll animations via IntersectionObserver (fade-up on enter)
- Smooth hover transitions (`transition-all duration-300`)
- Mobile responsive (hamburger menu on mobile)
- Sticky navbar with backdrop-blur

### DON'T:
- NO bright saturated gradients or gradient text
- NO emoji icons — use Lucide icons only
- NO "revolutionary", "game-changing" marketing copy
- NO heavy shadows or busy patterns
- NO dark mode toggle
- NO `border-radius` > `rounded-2xl`
- NO cramped spacing or fonts below 14px

---

## Typography Scale

| Element | Font | Size | Weight | Color |
|---|---|---|---|---|
| Site name / Hero H1 | Frank Ruhl Libre | 72px | 700 | white |
| Hero tagline | Inter | 20px | 300 | #d4d0ca |
| Section H2 (dark bg) | Frank Ruhl Libre | 44px | 600 | white |
| Section H2 (light bg) | Frank Ruhl Libre | 44px | 600 | #111 |
| Card H3 titles | Inter | 20px | 600 | — |
| Body paragraph | Inter | 16px | 400 | #444, lh 1.8 |
| Body on dark bg | Inter | 16px | 400 | #aaa, lh 1.8 |
| Small gold labels | Inter | 12px | 500 | #c9a96e, uppercase, ls 0.1em |
| Nav links | Inter | 14px | 500 | white |
| Stat numbers | Frank Ruhl Libre | 48px | 700 | #c9a96e |
| Stat labels | Inter | 14px | 400 | #666 |
| CTA button primary | Inter | 15px | 600 | bg #c9a96e, text #111 |
| CTA button secondary | Inter | 15px | 500 | border white/30, text white |
| Blog post date/tag | Inter | 12px | 500 | uppercase, #c9a96e |

---

## Color Palette

| Variable | Value | Usage |
|---|---|---|
| `--gold` | `#c9a96e` | Accent — borders, icons, labels, CTAs |
| `--dark` | `#111111` | Hero + dark sections background |
| `--light` | `#faf8f5` | Light sections background |
| Dark card bg | `#1a1a1a` | Practice area cards |
| Footer bg | `#0a0a0a` | Footer |

---

## Blog CMS
- Posts stored in `_posts/` as Markdown with YAML frontmatter
- Fields: `title`, `date`, `category`, `excerpt`, `body`, `published`
- Categories: נדל״ן | דיני משפחה | דיני חברות | ליטיגציה | כללי
- Admin panel at `/admin` (Decap CMS)
- After deploy: enable Netlify Identity + Git Gateway in Netlify dashboard

---

## Post-Deploy Netlify Setup (manual)
1. Site Settings → Identity → Enable Identity
2. Site Settings → Identity → Services → Enable Git Gateway
3. Site Settings → Identity → Invite users → enter Yair's email

Admin URL: `[SITE_URL]/admin`
