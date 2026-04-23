Gowanus Art Spine Webpage
This plan outlines the transformation of the Astro starter kit into a highly engaging, single-page presentation for the Gowanus Art Spine project. The focus will be on condensing the PDF content into a flowing narrative, creating a custom "artsy" aesthetic with sharp corners and uneven shapes, and building a "wow factor" interactive map to illustrate the impacts of congestion relief.

User Review Required
IMPORTANT

Please review the proposed artsy aesthetic and interactive map approach. Since you requested hand-drawn, uneven shapes and sharp corners, I plan to use custom CSS clips and SVG filters rather than standard web UI (no rounded corners or soft drop shadows).

Also, for the interactive map, I plan to build a custom SVG-based interactive component (or a highly stylized map using a mapping library) so that it matches the hand-drawn aesthetic better than a generic Google Map. Does this sound good?

Open Questions
WARNING

Images: You mentioned pulling in specific image files. Please provide/upload the images you want to use! Specifically, I'm looking for:
The map/route of the Gowanus Art Spine.
Simulation charts/visuals (e.g., the charts showing studio visits and commuter traffic).
Any hand-drawn or artistic assets you used in the presentation to enhance the vibe.
Map Interactivity: For the interactive map, do you want users to be able to click on the 4 different simulation scenarios (Studio Density, Awareness, Commuters, etc.) and see the map update, or should it be a map where they click on specific "studios" or "anchors" along the spine?
Proposed Changes
1. Astro Configuration & Setup
Clean up the default Astro blog starter files (remove blog posts, default layouts, etc.).
Setup global CSS (src/styles/global.css) to enforce the new design system (typography, sharp borders, uneven clip-paths).
2. Design System & Aesthetic (CSS)
[NEW] src/styles/global.css
Colors: Vibrant but slightly gritty palette (e.g., sharp black borders, high-contrast neons or rich earthy tones inspired by Gowanus).
Typography: Bold, structural headings (e.g., a brutalist or marker-style font) paired with a clean, readable body font.
Shapes: CSS clip-path and transform: skew() utilities to create elements that look slightly tilted or cut with scissors. Absolutely border-radius: 0 everywhere.
3. Components
[NEW] src/components/InteractiveMap.astro (or React/Svelte if state is complex)
A highly stylized interactive component.
It will feature the Gowanus spine. Users can toggle the "Congestion Relief" scenarios to see how foot traffic and studio visits change dynamically (using CSS animations or basic JS).
[NEW] src/components/ArtsySection.astro
Reusable wrapper component for different sections of the presentation to apply the uneven, sharp-edged container styles consistently.
[NEW] src/components/Timeline.astro
A visual timeline for the 4-phase Public Engagement Strategy (Listening Sessions -> Design -> Pilot -> Implementation).
4. Main Page Structure
[MODIFY] src/pages/index.astro
Hero: Impactful title ("The Gowanus Art Spine") with a striking background.
Context: Brief overview of congestion pricing and the gentrification challenge.
The Intervention (The Map): The "wow factor" InteractiveMap component showing the 4 scenarios.
Consensus & Timeline: The timeline component detailing the public engagement strategy.
Gowanus vs Highline: A sharp, contrasting section highlighting how this project avoids the pitfalls of the Highline.
Verification Plan
Automated Tests
Run npm run build to ensure the Astro site compiles without errors.
Run npm run dev and verify there are no console errors.
Manual Verification
Review the site in a local browser to ensure the aesthetic meets the "artsy, hand-drawn, sharp corners" requirements.
Test the Interactive Map to ensure hover/click states work and effectively communicate the simulation data.
Ensure the narrative flow is compressed but captures all key points from the PDF.


user notes:

ok see @pictures/ for the images i added, it can be somewhat scrollable! just not as long as the slides were, keep these 4 steps in mind: insights, transformation, prediction, consensus