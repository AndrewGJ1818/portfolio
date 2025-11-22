# Color palette

The following section presents the color palette selected for this portfolio project. The entire palette is built using complementary colors derived from a single base color, `#5D769C`. A low saturation has been applied across all tones, as it better aligns with the visual concept intended for the project. This approach helps create a cohesive and visually balanced aesthetic while maintaining a subtle and refined look.

To ensure the illustration assets remain visually engaging despite the low saturation, a range of distinct hues has been selected across the palette. This careful variation introduces enough contrast and diversity to bring a colorful feel to the visuals, without compromising the soft and muted atmosphere. The result is a balanced composition where illustrations can stand out and add personality, while still feeling cohesive within the overall design.

![Color Palette](/docs/img/colorpalette.png)

# Fonts

The typographic system for this portfolio has been carefully designed to reinforce the visual narrative of the filing cabinet, where each section simulates a different type of document. Each chosen font fulfills a specific functional and expressive role within this idea, while maintaining overall harmony, legibility, and performance consistency across the entire website.

All fonts are served directly through the Google Fonts API to ensure optimal performance, automatic format delivery, and shared caching benefits across browsers. The property `font-display: swap` is applied to all imported families, preventing text invisibility during loading and allowing an immediate fallback display for better perceived performance (FOUT strategy).

The following families are used throughout the project:

- **[Dynalight.](https://fonts.google.com/specimen/Dynalight)** A decorative script font used exclusively in the Home section, where it appears on the diploma illustration that introduces the site. Dynalight was selected after evaluating other calligraphic options whose uppercase characters felt overly ornate and hindered readability. Its smoother letterforms preserve a handwritten aesthetic while maintaining clear legibility, making it ideal for a signature-like display use.

- **[Indie Flower.](https://fonts.google.com/specimen/Indie+Flower)** This handwriting-style font appears across all interface elements designed to resemble sticky notes, such as the Skills document, the navigation bar, and other annotations throughout the interface. Despite its handwritten nature, Indie Flower was chosen for its exceptional legibility and balanced proportions, allowing it to convey a casual, personal tone without compromising clarity.

- **[PT Serif.](https://fonts.google.com/specimen/PT+Serif)** Used exclusively in the About Me document and the Home section, which is structured as a stack of papers containing longer passages of text. Its traditional serif design and high readability at paragraph scale help convey a sense of formality, professionalism, and textual density—ideal for representing an “official report” within the filing cabinet narrative.

- **[Roboto.](https://fonts.google.com/specimen/Roboto)** The main sans-serif family used across the Projects, Contact, and Footer sections, as well as other general text elements. Roboto’s geometric yet friendly shapes provide a neutral and modern tone that complements the more expressive fonts used elsewhere. It ensures high readability in all screen sizes and serves as the typographic foundation of the portfolio.

To improve performance, only the required weights (regular and bold) are loaded for each family, and the use of preconnect directives ensures faster resource fetching from Google’s CDN. Each section of the website uses a single primary font to preserve typographic consistency within that “document,” while maintaining visual distinction between sections.

# Design software

The design and illustration process for this portfolio was carried out entirely using [Inkscape](https://inkscape.org/), an open-source vector graphics editor. Inkscape was chosen for its flexibility, precision, and compatibility with scalable design workflows, making it an ideal tool for creating clean and adaptable visual assets.

All portfolio illustrations were designed as vector graphics within Inkscape, ensuring that each element could be easily resized and adjusted without any loss of quality. To support responsive design across different devices and screen resolutions, every illustration was exported in three distinct resolutions (referred as small, medium and large). This approach allows the visual assets to maintain clarity, proportion, and aesthetic consistency whether displayed on mobile, tablet, or desktop layouts.
