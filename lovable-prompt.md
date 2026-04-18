# Covenant Capital — Full Website Build (Lovable Prompt)

Build a complete business funding website for **Covenant Capital** — a business funding and partner program company. This should be a modern, luxurious single-page website with additional routes for privacy policy, terms, and a partner program page. Use React, TypeScript, Tailwind CSS, shadcn/ui, Framer Motion for animations, and Lucide icons.

## Brand Details

- **Company Name:** Covenant Capital
- **Founder:** Seung Hong
- **Phone:** (206) 466-0419
- **Email:** sthfinancialllc@gmail.com
- **Legal Entity:** STH Financial LLC
- **Tagline:** "Your Guides From Start to Funded"
- **Color Scheme:** Deep navy blue (#0a1628, #0f1d32, #162544) as backgrounds with rich gold/bronze (#c9a84c, #d4b65a, #a08530) as the accent/primary color. This is a luxe, premium financial look.
- **Fonts:** Playfair Display for headings, Inter for body text (import from Google Fonts)
- **Logo:** Use an SVG text-based logo. Show a small cross/shield icon (use Lucide `ShieldCheck` icon) next to the text "COVENANT" in the navbar. The logo should be gold on dark background. Style it to look premium and financial.

## Design System (CSS Variables)

Use these HSL-based CSS custom properties (dark theme ONLY, no light mode needed):

```css
:root {
  --background: 218 45% 7%;
  --foreground: 45 30% 95%;
  --gold: 43 54% 54%;
  --gold-light: 45 60% 62%;
  --gold-dark: 40 50% 38%;
  --card: 218 40% 10%;
  --card-foreground: 45 30% 95%;
  --popover: 218 42% 8%;
  --popover-foreground: 45 30% 95%;
  --primary: 43 54% 54%;
  --primary-foreground: 218 45% 7%;
  --secondary: 218 35% 14%;
  --secondary-foreground: 45 30% 95%;
  --muted: 218 30% 18%;
  --muted-foreground: 218 15% 55%;
  --accent: 43 54% 54%;
  --accent-foreground: 218 45% 7%;
  --destructive: 0 84% 60%;
  --destructive-foreground: 0 0% 100%;
  --border: 218 25% 22%;
  --input: 218 30% 18%;
  --ring: 43 54% 54%;
  --radius: 0.5rem;
}
```

Create these utility classes:
- `.text-gradient-gold` — gold gradient text (gold to gold-light to gold)
- `.bg-gradient-gold` — gold gradient background (gold to gold-light to gold-dark)
- `.bg-gradient-hero` — dark navy gradient for hero sections
- `.bg-gradient-card` — subtle dark card gradient
- `.glass-card` — frosted glass navbar effect (dark navy with blur)
- `.shadow-gold` — gold-tinted box shadow
- `.shadow-elegant` — deep shadow for cards

## Page Structure

### Routes:
- `/` — Main landing page (Index)
- `/privacy-policy` — Privacy Policy
- `/terms-and-conditions` — Terms & Conditions
- `/partner` — Partner Program signup page
- `/partner/thank-you` — Thank you page after partner signup
- `/sms-consent` — SMS consent info page

### Main Page Sections (in order):

#### 1. Navbar (fixed, glass effect)
- Logo on left (ShieldCheck icon + "COVENANT" text in gold, styled premium)
- Nav links: Home, Funding Products (with dropdown listing the products), Industries, Partners, Success Stories
- Right side: "Become a Partner" ghost button + "Apply Now" gold gradient button
- Mobile: hamburger menu with all links
- Glass morphism background with blur

#### 2. Hero Section
- Full viewport height, centered content
- Decorative circles with gold/primary glow in background (subtle, blurred)
- Badge: "Your Guides From Start to Funded"
- Main headline: `Reimagine The Way You` + `Access Capital` (gold gradient text)
- Subtext: "Get a quote with 1 application, access 300+ lenders, and receive multiple offers. Whether you need funding for your business or want to start your own funding company, Covenant Capital has you covered."
- Two CTA cards side by side:
  - **Get Funding** card — Building2 icon, gold gradient icon box, "Access up to $10M+ in business funding with competitive rates and flexible terms. Get funded in as little as 24-48 hours." + "Apply Now" gold button
  - **Start Your Own Business** card — Users icon, "Launch your own credit repair/funding company with our Done-For-You system. 100% fulfillment handled for you." + "Learn More" outline button
- Stats bar at bottom: 300+ Lending Partners | 5000+ Financial Products | $10M+ Funding Available | 24-48hrs Funding Speed
- All content uses Framer Motion staggered fade-up animations

#### 3. Funding Steps (4 steps)
- Section badge: "Simple Process"
- Heading: "Four Simple Steps to **Funding**" (gold)
- 4 cards in a row:
  1. Apply Online — "Fill out our 5 min application and tell us about your business"
  2. Meet Your Advisor — "Your advisor will review your options and discuss tailored solutions"
  3. Customized Plan — "Get a funding proposal with competitive rates and flexible terms"
  4. Get Funded — "Once approved, receive funds in as soon as 24-48 hours"
- Each has a step number (01-04), gold gradient icon box, connector lines between cards on desktop
- Icons: FileText, UserCheck, ClipboardCheck, Banknote

#### 4. Industries Section
- Badge: "Industries We Serve"
- Heading: "Customized Funding Solutions for **1000's of Industries**" (gold)
- 7 industry cards + 1 CTA card in a grid:
  - E-Commerce & Retail (ShoppingCart)
  - Real Estate (Building)
  - Trucking & Logistics (Truck)
  - Construction (HardHat)
  - Restaurants (UtensilsCrossed)
  - Landscaping (Trees)
  - Consultants & Agencies (Briefcase)
  - CTA card: "Don't See Your Industry?" with gold background + "Pre-Qualify Now" button
- Cards hover up slightly with border color change

#### 5. Products Section
- Badge: "Funding Products"
- Heading: "Access Over **5000+ Lending Products**" (gold)
- 8 product cards in a responsive grid:
  1. Business Line of Credit — Up to $1,000,000
  2. 0% Strategic Financing — $5,000 - $300,000+
  3. Business Term Loans — Up to $5 Million
  4. SBA Loans — Up to $10 Million
  5. Revenue-Based Financing — Up to $10 Million
  6. Start-Up/Working Capital — Flexible Amounts
  7. Equipment Financing — Up to $5 Million
  8. Real Estate / DSCR Loans — Up to $10 Million+
- Each card has: icon (gold gradient box), amount badge (top right), title, description
- Hover: glow overlay + lift animation
- CTA button below: "Check Your Eligibility" + note: "*Applying is free and won't impact your credit - 700+ credit score required"

#### 6. Partner Section
- Badge: "Partner Program"
- Heading: "Start Your Own **Funding Business**" (gold)
- Subtext: "Team up with Covenant Capital to grow your business and give your clients access to the financial solutions they need. 100% fulfillment done for you!"
- Two columns:
  - Left: "The Done-For-You Funding System" card with checklist: Complete business system ready to deploy, Marketing materials and lead generation, Full training and ongoing support, We handle all the fulfillment for you, Competitive commission structure. "Get Access Now" gold button linking to /partner
  - Right: 4 benefit cards (Access to 300+ Lenders, Dedicated Support, Unmatched Earning Potential, Exclusive Rewards) + "Who We Partner With" tag cloud (Accountants, Real Estate Agents, Credit Repair Companies, Insurance Brokers, Wholesale Distributors, Content Publishers, Consultants & Agencies)

#### 7. Testimonials Section
- Badge: "Testimonials"
- Heading: "Hear From Our **Amazing Clients**" (gold)
- 3 testimonial cards with 5-star ratings, quote, author name, title, funding amount badge
- Then "Proud To Be Part of Their **Journey**" with 3 success story cards (each has industry, title, need, solution, result, gold gradient top bar)
- Use the SAME testimonials and success stories as AOS Funds but with generic enough branding (no AOS mentions)

#### 8. Application Form
- Badge: "Get Started"
- Heading: "Your Guides From **Start to Funded**" (gold)
- Subtext: "1 application • 300+ Lenders • Multiple Offers"
- Form fields: Funding Amount (dropdown), Full Name, Email, Phone, Credit Score (dropdown), Business Address
- SMS consent checkbox with text: "By checking this box, I consent to receive SMS messages from Covenant Capital regarding my funding application, account updates, and related notifications. Message frequency varies. Msg & data rates may apply. Reply STOP to unsubscribe or HELP for help."
- Submit button: "Check Eligibility" gold gradient
- Trust badges: "Your information is secure" | "No impact on credit score" | "700+ credit score required"
- Links to Privacy Policy and Terms
- **Form submission:** For now, just show a toast notification "Thanks — we received your info. A funding advisor will contact you within 24 hours." (No Supabase or Zapier integration yet — we'll add those later)
- Include honeypot field (hidden) and basic rate limiting in a custom hook

#### 9. Footer
- Logo (same as navbar)
- Description: "Your guides from start to funded. Reimagine the way you access capital with 300+ lending partners and 5000+ financial products."
- Contact info: sthfinancialllc@gmail.com, (206) 466-0419, United States
- Three link columns: Funding Products, Company, Resources
- Bottom bar: "© 2026 STH Financial LLC. All rights reserved."
- No social media links for now (leave space for them)

### Partner Page (/partner)
- Navbar + Footer same as main page
- Hero section with "Launch Your **Funding Business** Today" heading
- Description about the Done-For-You system
- Benefits grid (6 items): Built-In Lender Network, Done-For-You Fulfillment, Training & Support, Your Own Brand, High Commissions, Proven System
- Simple partner signup form: Full Name, Email, Phone, Company Name, checkbox for terms agreement
- "Get Started Now" button — on submit, show toast "Application received! Our team will reach out within 24 hours." and redirect to /partner/thank-you
- FAQ accordion section with common partner questions

### Privacy Policy & Terms Pages
- Standard legal pages with Covenant Capital / STH Financial LLC branding
- Navbar + Footer included
- Professional formatting with proper sections
- Privacy Policy should mention: data collection, SMS communications, third-party sharing, data retention, contact info
- Terms should mention: service description, user responsibilities, limitation of liability, governing law

## Technical Requirements
- All animations with Framer Motion (fade up, stagger, hover effects)
- Fully responsive (mobile-first)
- Smooth scroll behavior
- Rate limiting hook for form submissions
- Honeypot bot protection on all forms
- Toast notifications for form feedback
- React Router for page navigation
- All components properly typed with TypeScript
- Use shadcn/ui components (Button, Input, Label, Select, Checkbox, Accordion, Toaster)
- SEO: proper title tag "Covenant Capital | Business Funding & Partner Program"

## Important Notes
- This is NOT AOS Funds — it is Covenant Capital, a separate company. Do not reference AOS anywhere.
- The founder is Seung Hong. The legal entity is STH Financial LLC.
- Keep the exact same professional quality, animations, and premium feel.
- The color scheme shifts from pure black backgrounds (AOS) to deep navy blue backgrounds (Covenant) — this matches Seung's existing branding card design.
- Gold remains the accent color but should be slightly more muted/bronze to match his card.
