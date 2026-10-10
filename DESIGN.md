# Portfolio Design Spec

> Working concept: **Personal Security Research Interface** — an editorial portfolio for cybersecurity, reverse engineering, and software security.

## Goals
- Present real projects and technical learning clearly to recruiters and technical teams.
- Feel visually distinctive without relying on generic “hacker” clichés.
- Keep content, accessibility, performance, and usability ahead of decorative effects.
- Build incrementally with AI assistance while retaining maintainable, understandable code.

## Art direction
**Keywords:** editorial, research lab, technical archive, restrained, experimental, precise.

**Visual principles**
- Strong editorial typography and clear hierarchy.
- Dark, near-black foundation with restrained neutral contrast; choose any accent only after contrast testing.
- Grids, fine rules, metadata labels, and compact technical annotations.
- Intentional negative space and selective asymmetry.
- Motion should establish hierarchy or explain interaction, not merely decorate.
- The page should feel like a security researcher’s personal space, not a SaaS landing-page template.

**Avoid**
- Purple/blue gradients as a default visual shortcut.
- Excessive glassmorphism, glowing cards, rounded rectangles, floating blobs, and particles.
- Matrix rain and generic terminal-themed layouts.
- Stock photos that do not serve a real content purpose.
- Generic “passionate developer” copy or invented metrics, credentials, results, or experience.
- Animating every element or making core content inaccessible without animation.

## Inspiration board
These are references for specific design decisions, not templates to copy.

### Identity and layout
- [Hacktron AI](https://www.hacktron.ai/) — cybersecurity/research identity, technical details, diagnostic-panel idea.
- [ThreeUI browse](https://threeui.com/browse?sort=recent) — discover individual visual components and page concepts.
- [sublevel.studio on ThreeUI](https://threeui.com/landing-pages/sublevel-studio-landing-page) — OS/lab-inspired information architecture and modular project presentation.
- [Mara Voss on ThreeUI](https://threeui.com/landing-pages/mara-voss-landing-page) — editorial archive / research specimen approach.
- [RenderLab on ThreeUI](https://threeui.com/landing-pages/renderlab-landing-page) — grid, cursor label, scroll progress, and layout details.
- [Taste Skill](https://www.tasteskill.dev/) — reminder to challenge generic AI-generated frontend patterns.

### Motion and components
- [GSAP](https://gsap.com/) — controlled entrance, scroll, and micro-interaction motion.
- [21st.dev](https://21st.dev/) — component discovery; review source, dependencies, licence/usage terms, and maintenance before using components.
- [ThreeUI Pixel Terminal Dock](https://threeui.com/css/animated-top-dock/retro) — possible navigation inspiration; adapt rather than copy wholesale.
- [ThreeUI CRT Terminal](https://threeui.com/backgrounds/crt/terminal) — optional small boot/status detail, not a full-page treatment.
- [ThreeUI Glitch Fall](https://threeui.com/text-animation/gallery-heading/falling-diagonal) — optional, rare heading accent only.

### Hero visual: Optimized Black Hole
- Source: [21st.dev](https://21st.dev/) — component supplied by the project owner.
- Intended use: atmospheric visual behind the hero copy.
- Status: **not integrated yet**. The supplied snippet imports `./optimized-black-hole-utils/renderer`, so all renderer and utility source files must be retrieved before implementation. Do not invent missing utilities or assume the snippet is self-contained.
- Fallback: render the hero without the effect if the complete source, usage terms, or acceptable performance cannot be established.
- Requirements: canvas must not block navigation or links; manage renderer lifecycle; resize correctly; respect reduced motion; test on mobile and provide a graceful fallback.

## Proposed site architecture
1. **Hero** — name, accurate positioning, concise statement, primary links.
2. **Selected work** — only real projects, with objective, role, technology, challenges, and repository links.
3. **Research / field notes** — technical write-ups and learning notes.
4. **About** — concise background and current interests.
5. **Technical toolkit** — distinguish active skills from topics being learned.
6. **Current focus / system status** — optional, truthful, maintained metadata.
7. **Contact** — GitHub, LinkedIn, and an approved contact method.

Sections and copy are proposals; confirm before publishing professional claims.

## Content rules
- Never invent job experience, client work, certifications, achievements, benchmarks, or project outcomes.
- Do not publish secrets, private data, sensitive exploit details, or proprietary materials.
- Clearly distinguish personal learning projects from professional experience.
- Link project cards to real repositories or write-ups when they exist.
- Prefer specific explanations over hype.

## Technical approach (provisional)
- Use a static-first React + TypeScript build so GitHub Pages remains a viable zero-cost hosting option.
- Tailwind CSS and a shadcn-compatible component structure are candidates, not requirements; confirm the scaffold before installing anything.
- Keep animation and WebGL dependencies isolated. Add GSAP or Three.js only where a concrete interaction needs it.
- Avoid features that require a server at runtime unless deployment plans change.
- Add an appropriate .gitignore, lockfile, accessible semantic markup, and repeatable build instructions when the app is scaffolded.

## Quality bar
Before deployment:
- Run a production build and available tests.
- Check responsive layouts, keyboard interaction, focus visibility, color contrast, and reduced-motion behavior.
- Check links, metadata, page titles, favicon, and missing assets.
- Review dependencies and check for accidentally committed secrets.
- Inspect console/build errors and performance on a mobile-sized viewport.
- Document unresolved issues; do not claim the site is error-free without verification.

## Decisions still to make
- Final framework/build tool and GitHub Pages deployment path.
- Final typography and accent color.
- Complete source and usage conditions of the Optimized Black Hole component.
- Which projects and write-ups are ready to feature.
- Which external profiles and contact details should be public.

## Build sequence
1. Agree on this spec and refine preferences.
2. Gather the exact references/screenshots that matter.
3. Select the static site scaffold and verify its build locally.
4. Implement the static hero and page structure.
5. Integrate the black-hole effect only after the static design works.
6. Add motion selectively.
7. Add verified project content.
8. Test accessibility, responsiveness, security basics, SEO, and performance.
9. Configure GitHub Pages and verify the deployed site.
