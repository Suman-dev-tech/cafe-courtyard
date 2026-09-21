# Cafe Courtyard — Digital Continental Food Journal

## 1. Project Description

Cafe Courtyard is a premium café in New Town, Kolkata, India. This website reimagines the café not as a traditional restaurant site but as a digital continental food journal and community platform. The café acts as the host and curator of conversations, food stories, cultural discussions, and culinary experiences.

**Positioning:** A premium editorial magazine meets European café culture meets slow living journal. Visitors come to explore stories, participate in conversations about continental cuisine, and discover food culture before ever seeing a menu.

**Target Users:** Food enthusiasts, continental cuisine lovers, Kolkata locals and visitors, people interested in food culture and storytelling.

**Core Value:** Every dish has a story. Every table hosts a conversation. The café is a living journal of continental food culture.

## 2. Page Structure

| Route | Page | Description |
|-------|------|-------------|
| `/` | Homepage | Hero, Featured Story, Conversations, Signature Dishes, Latest Articles, Community Highlights, About preview, Visit preview |
| `/journal` | The Courtyard Journal | Editorial magazine listing with categories: Food Stories, Continental Culture, Chef Diaries, Travel & Taste, Community Voices |
| `/journal/:slug` | Article Detail | Long-form editorial article with hero image, author, reading time, pull quotes, related stories, discussion prompt |
| `/the-table` | The Table | Story-driven menu: Chef's Signature, Community Favourites, Seasonal Specials, Coffee Collection, Sweet Endings |
| `/dish/:slug` | Dish Detail | Editorial dish page with origin story, ingredients, chef notes, pairings, related stories |
| `/community` | Community Table | Discussion hub: Discussion of the Week, Food Questions, Community Opinions, Featured Conversations, Food Polls |
| `/about` | About Cafe Courtyard | Our Story, Philosophy, Community Vision, The Courtyard Experience |
| `/founder` | Founder Story | Sudarshana Dutt's journey and inspiration — visual narrative timeline |
| `/gallery` | Gallery | Magazine-style visual storytelling: Food, People, Events, The Space, Moments |
| `/visit` | Visit Us | Location, Timings, Reservations, Contact, Map, Social Media |

## 3. Core Features

- [ ] Editorial homepage with immersive hero, story sections, dish highlights, community preview
- [ ] Magazine-style journal with category navigation and article cards
- [ ] Full article reading experience with editorial typography and pull quotes
- [ ] Story-driven "The Table" menu (not traditional pricing-first menu)
- [ ] Dish detail pages with origin stories, chef notes, pairing suggestions
- [ ] Community discussion hub with conversation cards and food polls
- [ ] About and Founder story pages with visual narrative
- [ ] Magazine-style gallery with category filtering
- [ ] Visit us page with location, contact, and reservation info
- [ ] Newsletter subscription form
- [ ] Responsive navigation with hamburger on mobile
- [ ] Contact form integration

## 4. Data Model Design

This project uses mock data (no Supabase connected initially). All content is stored in `src/mocks/` as static data files for immediate rich visual experience.

When Supabase is connected later, data migration path:
- Articles table: id, title, slug, category, excerpt, content, author, image, reading_time, created_at, featured
- Dishes table: id, name, slug, category, story, origin, ingredients, chef_notes, pairings, image, featured
- Community discussions table: id, title, excerpt, category, author, responses_count, created_at
- Gallery items table: id, title, category, image, description

## 5. Backend / Third-party Integration Plan

- **Supabase:** Not required for Phase 1-4. Can be connected later for dynamic content management if needed.
- **Shopify:** Not needed — this is not an e-commerce menu.
- **Stripe:** Not needed — no online payments.
- **Form submissions:** Use Readdy's built-in form system for newsletter and contact forms.

## 6. Development Phase Plan

### Phase 1: Foundation + Homepage ✓
- Goal: Establish design system, routing, shared components, and build the complete homepage
- Deliverable: Full homepage with hero, featured stories, community preview, signature dishes, latest articles, about preview, visit preview, navbar, footer
- **Redesigned:** Hero centered with one CTA, café façade background. Philosophy quote transition. Our Roots two-column with founder. Plate Stories before Flavor Files. Flavor Files simplified to 2 cards. Pinterest-style masonry gallery (The Frame). Reordered footer with bougainvillea illustration.

### Phase 2: Journal + Article Detail
- Goal: Build the editorial journal experience
- Deliverable: `/journal` listing page and `/journal/:slug` article detail page with editorial layout

### Phase 3: The Table (Menu) + Dish Detail
- Goal: Build story-driven menu and dish pages
- Deliverable: `/the-table` menu page and `/dish/:slug` dish detail page

### Phase 4: Community + About + Gallery + Visit
- Goal: Complete all remaining pages
- Deliverable: `/community`, `/about`, `/founder`, `/gallery`, `/visit` pages

### Phase 5: Polish & Interactions ✓ (partial)
- Goal: Add animations, refine responsive behavior, form integrations, final polish
- Deliverable: ~~Smooth scroll animations~~ (added IntersectionObserver fade-in), refined mobile experience, newsletter form, contact form, final QA