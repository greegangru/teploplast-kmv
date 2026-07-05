# Penoplast KMV SEO Expansion Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Перенести текущий статический сайт в рабочую папку, усилить главную страницу под коммерческие SEO-запросы КМВ и добавить 5 уникальных городских страниц для роста локального поиска и звонков.

**Architecture:** Базой остаётся статический HTML-сайт без зависимостей. Главная страница сохраняет роль основного коммерческого URL по региону КМВ, а отдельные страницы городов получают уникальные мета-теги, контент, FAQ, schema и перелинковку. Общие ассеты используются повторно, а структура сайта расширяется через новые директории и обновлённую карту сайта.

**Tech Stack:** Статический HTML, inline CSS/JS, XML sitemap, robots.txt, schema.org JSON-LD

---

## File Structure

**Create:**
- `C:\Users\111\Documents\пенопласт\index.html`
- `C:\Users\111\Documents\пенопласт\apple-touch-icon.png`
- `C:\Users\111\Documents\пенопласт\favicon.ico`
- `C:\Users\111\Documents\пенопласт\favicon.svg`
- `C:\Users\111\Documents\пенопласт\icon-192.png`
- `C:\Users\111\Documents\пенопласт\icon-512.png`
- `C:\Users\111\Documents\пенопласт\og-cover.png`
- `C:\Users\111\Documents\пенопласт\site.webmanifest`
- `C:\Users\111\Documents\пенопласт\robots.txt`
- `C:\Users\111\Documents\пенопласт\sitemap.xml`
- `C:\Users\111\Documents\пенопласт\pyatigorsk\index.html`
- `C:\Users\111\Documents\пенопласт\essentuki\index.html`
- `C:\Users\111\Documents\пенопласт\kislovodsk\index.html`
- `C:\Users\111\Documents\пенопласт\mineralnye-vody\index.html`
- `C:\Users\111\Documents\пенопласт\zheleznovodsk\index.html`

**Modify:**
- `C:\Users\111\Documents\пенопласт\docs\superpowers\specs\2026-07-05-penoplast-kmv-seo-design.md` only if implementation reveals a spec inconsistency

**Reference Source:**
- `C:\Users\111\Desktop\TG\penoplast-kmv\index.html`
- `C:\Users\111\Desktop\TG\penoplast-kmv\robots.txt`
- `C:\Users\111\Desktop\TG\penoplast-kmv\sitemap.xml`

### Task 1: Import The Existing Site Into The Workspace

**Files:**
- Create: `C:\Users\111\Documents\пенопласт\index.html`
- Create: `C:\Users\111\Documents\пенопласт\apple-touch-icon.png`
- Create: `C:\Users\111\Documents\пенопласт\favicon.ico`
- Create: `C:\Users\111\Documents\пенопласт\favicon.svg`
- Create: `C:\Users\111\Documents\пенопласт\icon-192.png`
- Create: `C:\Users\111\Documents\пенопласт\icon-512.png`
- Create: `C:\Users\111\Documents\пенопласт\og-cover.png`
- Create: `C:\Users\111\Documents\пенопласт\site.webmanifest`
- Create: `C:\Users\111\Documents\пенопласт\robots.txt`
- Create: `C:\Users\111\Documents\пенопласт\sitemap.xml`

- [ ] **Step 1: Copy the existing static site files into the workspace**

Run:

```powershell
Copy-Item -LiteralPath 'C:\Users\111\Desktop\TG\penoplast-kmv\index.html' -Destination 'C:\Users\111\Documents\пенопласт\index.html'
Copy-Item -LiteralPath 'C:\Users\111\Desktop\TG\penoplast-kmv\apple-touch-icon.png' -Destination 'C:\Users\111\Documents\пенопласт\apple-touch-icon.png'
Copy-Item -LiteralPath 'C:\Users\111\Desktop\TG\penoplast-kmv\favicon.ico' -Destination 'C:\Users\111\Documents\пенопласт\favicon.ico'
Copy-Item -LiteralPath 'C:\Users\111\Desktop\TG\penoplast-kmv\favicon.svg' -Destination 'C:\Users\111\Documents\пенопласт\favicon.svg'
Copy-Item -LiteralPath 'C:\Users\111\Desktop\TG\penoplast-kmv\icon-192.png' -Destination 'C:\Users\111\Documents\пенопласт\icon-192.png'
Copy-Item -LiteralPath 'C:\Users\111\Desktop\TG\penoplast-kmv\icon-512.png' -Destination 'C:\Users\111\Documents\пенопласт\icon-512.png'
Copy-Item -LiteralPath 'C:\Users\111\Desktop\TG\penoplast-kmv\og-cover.png' -Destination 'C:\Users\111\Documents\пенопласт\og-cover.png'
Copy-Item -LiteralPath 'C:\Users\111\Desktop\TG\penoplast-kmv\site.webmanifest' -Destination 'C:\Users\111\Documents\пенопласт\site.webmanifest'
Copy-Item -LiteralPath 'C:\Users\111\Desktop\TG\penoplast-kmv\robots.txt' -Destination 'C:\Users\111\Documents\пенопласт\robots.txt'
Copy-Item -LiteralPath 'C:\Users\111\Desktop\TG\penoplast-kmv\sitemap.xml' -Destination 'C:\Users\111\Documents\пенопласт\sitemap.xml'
```

- [ ] **Step 2: Verify that the imported files exist in the workspace**

Run:

```powershell
Get-ChildItem -Force 'C:\Users\111\Documents\пенопласт'
```

Expected: `index.html`, asset files, `robots.txt`, `sitemap.xml`, and the existing `docs` directory are present.

- [ ] **Step 3: Commit the imported baseline**

```bash
git add index.html apple-touch-icon.png favicon.ico favicon.svg icon-192.png icon-512.png og-cover.png site.webmanifest robots.txt sitemap.xml
git commit -m "chore: import penoplast kmv site baseline"
```

### Task 2: Strengthen The Main Page SEO Structure

**Files:**
- Modify: `C:\Users\111\Documents\пенопласт\index.html`

- [ ] **Step 1: Write the updated main-page SEO content into a temporary checklist**

Apply this exact content intent while editing `index.html`:

```text
Title: Купить фасадный пенопласт в КМВ от производителя | Пенопласт 25 плотности | ТеплоПласт КМВ
Description: Купить фасадный пенопласт в КМВ от производителя. Пенопласт 25 плотности для утепления фасадов, листы 1x1 и 1x2 м, любая толщина под заказ. Пятигорск, Ессентуки, Кисловодск, Минеральные Воды, Железноводск. Звоните: 8 903 408-78-40.
Hero focus: прямой производитель, цена от завода, быстрый расчёт, весь регион КМВ
New section focus: города КМВ, преимущества производителя, размеры и толщина, заказ и отгрузка
```

- [ ] **Step 2: Edit the main page head section and visible content**

Implement these exact changes:

```html
<title>Купить фасадный пенопласт в КМВ от производителя | Пенопласт 25 плотности | ТеплоПласт КМВ</title>
<meta name="description" content="Купить фасадный пенопласт в КМВ от производителя. Пенопласт 25 плотности для утепления фасадов, листы 1x1 и 1x2 м, любая толщина под заказ. Пятигорск, Ессентуки, Кисловодск, Минеральные Воды, Железноводск. Звоните: 8 903 408-78-40.">
<meta property="og:title" content="Купить фасадный пенопласт в КМВ от производителя | ТеплоПласт КМВ">
<meta property="og:description" content="Пенопласт 25 плотности от производителя в КМВ: Пятигорск, Ессентуки, Кисловодск, Минеральные Воды, Железноводск. Цена от завода, любая толщина под заказ.">
```

Also add or revise visible sections so the page contains:

```html
<section id="cities">
  <div class="container">
    <div class="section-head reveal">
      <span class="eyebrow">Города КМВ</span>
      <h2>Поставляем фасадный пенопласт по всему региону КМВ</h2>
      <p>Работаем по Пятигорску, Ессентукам, Кисловодску, Минеральным Водам и Железноводску. Для каждого города подготовлена отдельная страница с подробностями по заказу и поставке.</p>
    </div>
  </div>
</section>
```

- [ ] **Step 3: Expand schema on the main page**

Ensure the JSON-LD includes a `BreadcrumbList` block like this:

```json
{
  "@type": "BreadcrumbList",
  "@id": "https://teploplast-kmv.ru/#breadcrumbs",
  "itemListElement": [
    {
      "@type": "ListItem",
      "position": 1,
      "name": "Главная",
      "item": "https://teploplast-kmv.ru/"
    }
  ]
}
```

- [ ] **Step 4: Verify the updated main page contains the new target sections**

Run:

```powershell
Select-String -Path 'C:\Users\111\Documents\пенопласт\index.html' -Pattern 'Города КМВ|Пятигорск|Ессентуки|Кисловодск|Минеральные Воды|Железноводск|BreadcrumbList|Купить фасадный пенопласт в КМВ'
```

Expected: matches in the head metadata, visible city section, and JSON-LD.

- [ ] **Step 5: Commit the strengthened main page**

```bash
git add index.html
git commit -m "feat: strengthen penoplast kmv main page seo"
```

### Task 3: Create A Reusable Structure For City Pages

**Files:**
- Create: `C:\Users\111\Documents\пенопласт\pyatigorsk\index.html`
- Create: `C:\Users\111\Documents\пенопласт\essentuki\index.html`
- Create: `C:\Users\111\Documents\пенопласт\kislovodsk\index.html`
- Create: `C:\Users\111\Documents\пенопласт\mineralnye-vody\index.html`
- Create: `C:\Users\111\Documents\пенопласт\zheleznovodsk\index.html`

- [ ] **Step 1: Create the city directories**

Run:

```powershell
New-Item -ItemType Directory -Path 'C:\Users\111\Documents\пенопласт\pyatigorsk' -Force
New-Item -ItemType Directory -Path 'C:\Users\111\Documents\пенопласт\essentuki' -Force
New-Item -ItemType Directory -Path 'C:\Users\111\Documents\пенопласт\kislovodsk' -Force
New-Item -ItemType Directory -Path 'C:\Users\111\Documents\пенопласт\mineralnye-vody' -Force
New-Item -ItemType Directory -Path 'C:\Users\111\Documents\пенопласт\zheleznovodsk' -Force
```

- [ ] **Step 2: Build the first city page template with real SEO content**

Write `C:\Users\111\Documents\пенопласт\pyatigorsk\index.html` using the existing site’s visual system and this SEO frame:

```html
<title>Купить фасадный пенопласт в Пятигорске от производителя | ТеплоПласт КМВ</title>
<meta name="description" content="Купить фасадный пенопласт в Пятигорске от производителя. Пенопласт 25 плотности, листы 1x1 и 1x2 м, любая толщина под заказ. Прямые цены от завода. Телефон: 8 903 408-78-40.">
<link rel="canonical" href="https://teploplast-kmv.ru/pyatigorsk/">
<h1>Купить фасадный пенопласт в Пятигорске от производителя</h1>
<h2>Поставляем пенопласт в Пятигорск напрямую с производства</h2>
<h2>Размеры и толщина пенопласта для объектов в Пятигорске</h2>
<h2>Частые вопросы о заказе пенопласта в Пятигорске</h2>
```

- [ ] **Step 3: Create the remaining city pages with unique localized metadata**

Use these exact heads:

```html
<!-- essentuki/index.html -->
<title>Купить фасадный пенопласт в Ессентуках от производителя | ТеплоПласт КМВ</title>
<meta name="description" content="Купить фасадный пенопласт в Ессентуках от производителя. Пенопласт 25 плотности для утепления фасадов, прямая цена от завода, любая толщина под заказ. Телефон: 8 903 408-78-40.">
<link rel="canonical" href="https://teploplast-kmv.ru/essentuki/">

<!-- kislovodsk/index.html -->
<title>Купить фасадный пенопласт в Кисловодске от производителя | ТеплоПласт КМВ</title>
<meta name="description" content="Купить фасадный пенопласт в Кисловодске от производителя. Фасадный пенопласт 25 плотности, листы 1x1 и 1x2 м, прямая поставка по КМВ. Телефон: 8 903 408-78-40.">
<link rel="canonical" href="https://teploplast-kmv.ru/kislovodsk/">

<!-- mineralnye-vody/index.html -->
<title>Купить фасадный пенопласт в Минеральных Водах от производителя | ТеплоПласт КМВ</title>
<meta name="description" content="Купить фасадный пенопласт в Минеральных Водах от производителя. Пенопласт 25 плотности для утепления фасадов, любая толщина, прямые цены от завода. Телефон: 8 903 408-78-40.">
<link rel="canonical" href="https://teploplast-kmv.ru/mineralnye-vody/">

<!-- zheleznovodsk/index.html -->
<title>Купить фасадный пенопласт в Железноводске от производителя | ТеплоПласт КМВ</title>
<meta name="description" content="Купить фасадный пенопласт в Железноводске от производителя. Фасадный пенопласт для частных и коммерческих объектов, размеры 1x1 и 1x2 м, цена от завода. Телефон: 8 903 408-78-40.">
<link rel="canonical" href="https://teploplast-kmv.ru/zheleznovodsk/">
```

- [ ] **Step 4: Verify that all city pages exist**

Run:

```powershell
Get-ChildItem -Recurse -Filter index.html 'C:\Users\111\Documents\пенопласт\pyatigorsk','C:\Users\111\Documents\пенопласт\essentuki','C:\Users\111\Documents\пенопласт\kislovodsk','C:\Users\111\Documents\пенопласт\mineralnye-vody','C:\Users\111\Documents\пенопласт\zheleznovodsk'
```

Expected: one `index.html` file exists inside each city directory.

- [ ] **Step 5: Commit the city page scaffolding**

```bash
git add pyatigorsk/index.html essentuki/index.html kislovodsk/index.html mineralnye-vody/index.html zheleznovodsk/index.html
git commit -m "feat: add kmv city landing pages"
```

### Task 4: Add Unique FAQ, Local Schema, And Internal Linking To City Pages

**Files:**
- Modify: `C:\Users\111\Documents\пенопласт\pyatigorsk\index.html`
- Modify: `C:\Users\111\Documents\пенопласт\essentuki\index.html`
- Modify: `C:\Users\111\Documents\пенопласт\kislovodsk\index.html`
- Modify: `C:\Users\111\Documents\пенопласт\mineralnye-vody\index.html`
- Modify: `C:\Users\111\Documents\пенопласт\zheleznovodsk\index.html`

- [ ] **Step 1: Add a localized FAQ block to each city page**

Each page must contain at least these structures, adapted to the city:

```html
<section id="faq">
  <div class="container">
    <h2>Частые вопросы о покупке пенопласта в Пятигорске</h2>
    <details>
      <summary>Как заказать фасадный пенопласт в Пятигорске?</summary>
      <p>Позвоните по номеру 8 903 408-78-40, сообщите нужную толщину, площадь и формат листов. Мы рассчитаем стоимость и согласуем отгрузку.</p>
    </details>
    <details>
      <summary>Какой пенопласт подходит для утепления фасада в Пятигорске?</summary>
      <p>Для фасадных работ обычно выбирают пенопласт 25 плотности. Подберём толщину под ваш объект и задачу утепления.</p>
    </details>
  </div>
</section>
```

- [ ] **Step 2: Add local schema and breadcrumbs to each city page**

Each city page must contain JSON-LD blocks matching this structure:

```json
{
  "@context": "https://schema.org",
  "@graph": [
    {
      "@type": "BreadcrumbList",
      "itemListElement": [
        {"@type": "ListItem", "position": 1, "name": "Главная", "item": "https://teploplast-kmv.ru/"},
        {"@type": "ListItem", "position": 2, "name": "Пятигорск", "item": "https://teploplast-kmv.ru/pyatigorsk/"}
      ]
    },
    {
      "@type": "FAQPage"
    }
  ]
}
```

- [ ] **Step 3: Add internal links to the main page and other cities**

Insert a navigation block like this on every city page:

```html
<section class="city-links">
  <div class="container">
    <h2>Другие города КМВ</h2>
    <p><a href="/">Главная по КМВ</a> · <a href="/essentuki/">Ессентуки</a> · <a href="/kislovodsk/">Кисловодск</a> · <a href="/mineralnye-vody/">Минеральные Воды</a> · <a href="/zheleznovodsk/">Железноводск</a></p>
  </div>
</section>
```

- [ ] **Step 4: Verify unique city mentions and schema markers**

Run:

```powershell
Get-ChildItem -Recurse -Filter index.html 'C:\Users\111\Documents\пенопласт\pyatigorsk','C:\Users\111\Documents\пенопласт\essentuki','C:\Users\111\Documents\пенопласт\kislovodsk','C:\Users\111\Documents\пенопласт\mineralnye-vody','C:\Users\111\Documents\пенопласт\zheleznovodsk' | Select-String -Pattern 'BreadcrumbList|FAQPage|Главная по КМВ|Пятигорск|Ессентуки|Кисловодск|Минеральные Воды|Железноводск'
```

Expected: every page shows breadcrumb schema, FAQ schema, and internal links.

- [ ] **Step 5: Commit the city-page SEO enrichment**

```bash
git add pyatigorsk/index.html essentuki/index.html kislovodsk/index.html mineralnye-vody/index.html zheleznovodsk/index.html
git commit -m "feat: enrich kmv city pages with local seo content"
```

### Task 5: Update Sitewide Indexing Files

**Files:**
- Modify: `C:\Users\111\Documents\пенопласт\sitemap.xml`
- Modify: `C:\Users\111\Documents\пенопласт\robots.txt`

- [ ] **Step 1: Expand the sitemap with all city URLs**

Replace the sitemap contents with:

```xml
<?xml version="1.0" encoding="UTF-8"?>
<urlset xmlns="http://www.sitemaps.org/schemas/sitemap/0.9">
  <url>
    <loc>https://teploplast-kmv.ru/</loc>
    <lastmod>2026-07-05</lastmod>
    <changefreq>weekly</changefreq>
    <priority>1.0</priority>
  </url>
  <url>
    <loc>https://teploplast-kmv.ru/pyatigorsk/</loc>
    <lastmod>2026-07-05</lastmod>
    <changefreq>weekly</changefreq>
    <priority>0.9</priority>
  </url>
  <url>
    <loc>https://teploplast-kmv.ru/essentuki/</loc>
    <lastmod>2026-07-05</lastmod>
    <changefreq>weekly</changefreq>
    <priority>0.9</priority>
  </url>
  <url>
    <loc>https://teploplast-kmv.ru/kislovodsk/</loc>
    <lastmod>2026-07-05</lastmod>
    <changefreq>weekly</changefreq>
    <priority>0.9</priority>
  </url>
  <url>
    <loc>https://teploplast-kmv.ru/mineralnye-vody/</loc>
    <lastmod>2026-07-05</lastmod>
    <changefreq>weekly</changefreq>
    <priority>0.9</priority>
  </url>
  <url>
    <loc>https://teploplast-kmv.ru/zheleznovodsk/</loc>
    <lastmod>2026-07-05</lastmod>
    <changefreq>weekly</changefreq>
    <priority>0.9</priority>
  </url>
</urlset>
```

- [ ] **Step 2: Keep robots.txt simple and explicit**

Ensure `robots.txt` contains:

```txt
User-agent: *
Allow: /

Sitemap: https://teploplast-kmv.ru/sitemap.xml
```

- [ ] **Step 3: Verify sitemap and robots content**

Run:

```powershell
Get-Content -LiteralPath 'C:\Users\111\Documents\пенопласт\sitemap.xml'
Get-Content -LiteralPath 'C:\Users\111\Documents\пенопласт\robots.txt'
```

Expected: sitemap contains the homepage plus 5 city pages, and `robots.txt` points to the sitemap.

- [ ] **Step 4: Commit the indexing files**

```bash
git add sitemap.xml robots.txt
git commit -m "feat: update sitemap for kmv city pages"
```

### Task 6: Final Review And Verification

**Files:**
- Modify: `C:\Users\111\Documents\пенопласт\index.html`
- Modify: `C:\Users\111\Documents\пенопласт\pyatigorsk\index.html`
- Modify: `C:\Users\111\Documents\пенопласт\essentuki\index.html`
- Modify: `C:\Users\111\Documents\пенопласт\kislovodsk\index.html`
- Modify: `C:\Users\111\Documents\пенопласт\mineralnye-vody\index.html`
- Modify: `C:\Users\111\Documents\пенопласт\zheleznovodsk\index.html`
- Modify: `C:\Users\111\Documents\пенопласт\sitemap.xml`
- Modify: `C:\Users\111\Documents\пенопласт\robots.txt`

- [ ] **Step 1: Run a final keyword and structure verification pass**

Run:

```powershell
Select-String -Path 'C:\Users\111\Documents\пенопласт\index.html' -Pattern '<title>|meta name=\"description\"|canonical|BreadcrumbList|Города КМВ|Пятигорск|Ессентуки|Кисловодск|Минеральные Воды|Железноводск'
Get-ChildItem -Recurse -Filter index.html 'C:\Users\111\Documents\пенопласт\pyatigorsk','C:\Users\111\Documents\пенопласт\essentuki','C:\Users\111\Documents\пенопласт\kislovodsk','C:\Users\111\Documents\пенопласт\mineralnye-vody','C:\Users\111\Documents\пенопласт\zheleznovodsk' | Select-String -Pattern '<title>|meta name=\"description\"|canonical|BreadcrumbList|FAQPage|Главная по КМВ'
```

Expected: all pages include metadata, canonical, and internal linking markers.

- [ ] **Step 2: Manually review for duplicate city copy**

Check that each city page differs in:

```text
title
description
h1
FAQ wording
city-specific explanatory paragraph
```

Expected: no two city pages read like exact clones with only the city name swapped.

- [ ] **Step 3: Stage and commit the full SEO expansion**

```bash
git add index.html pyatigorsk/index.html essentuki/index.html kislovodsk/index.html mineralnye-vody/index.html zheleznovodsk/index.html sitemap.xml robots.txt
git commit -m "feat: expand penoplast kmv local seo structure"
```

## Self-Review

**Spec coverage:** The plan covers main-page strengthening, 5 city pages, internal linking, schema, sitemap, and robots updates from the approved spec.

**Placeholder scan:** No `TODO`, `TBD`, or abstract “handle later” steps remain; all tasks include exact files and commands.

**Type consistency:** Paths, page URLs, and city slugs are consistent across main page, city pages, and sitemap tasks.
