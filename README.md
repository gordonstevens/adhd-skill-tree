# ADHD Skill Tree Visualization

## Introduction

This project is an interactive, web-based visualization of strategies, strengths, and environmental supports related to managing ADHD. It uses a "skill tree" metaphor, inspired by video games, to present information in an engaging and interconnected way.

**Purpose:** To help users visualize and better understand various facets of ADHD management, including active coping strategies, commonly associated passive strengths, and helpful environmental setups.

**Disclaimer:** This is an informational visualization and **not** a diagnostic or treatment tool. The content is based on general information about ADHD management techniques and traits. Consult with qualified professionals for diagnosis and treatment.

## Features

* **Interactive Visualization:** Uses Three.js to create a dynamic, explorable skill tree in a 2D plane.
* **Categorized Skills:** Information is grouped into logical sections (e.g., Planning & Organization, Focus & Attention, Emotional Regulation, etc.).
* **Active vs. Passive Distinction:** Skills are color-coded (by default) to differentiate between active strategies requiring conscious effort and passive strengths/supports.
* **Visual Connections:** Lines are drawn between related skills/traits to show potential pathways or relationships.
* **Hover Interaction:** Hovering over a skill provides visual feedback (color change, slight scale) and displays a tooltip with its name, type, and description.
* **Clickable Links:** Clicking on a skill opens a corresponding explanation in a separate HTML file (`adhd-skill-tree-explanation.htm`) by linking to specific anchor tags. (One skill links to Google as an example).
* **Panning & Zooming:** Uses Three.js `OrbitControls` to allow users to pan (click/drag) and zoom (scroll/pinch) the view, making it usable even when content exceeds the screen size.
* **Theming:**
    * Supports both a Dark theme and a colourful "Alt" theme (dark blue base).
    * Automatically detects OS color preference (`prefers-color-scheme`) for the initial theme.
    * Includes a "Toggle Theme" button for manual override.
    * User theme preference is saved in `localStorage`.
* **Responsive Design:** The camera view and HTML overlays adjust to different screen sizes and zoom levels.
* **Single-File Structure:** The main visualization runs entirely from a single HTML file (`adhd-skill-tree.htm`), with explanations in a second linked HTML file (`adhd-skill-tree-explanation.htm`). No build process required.

## Technology Used

* HTML5
* CSS3 (including CSS Variables, Media Queries)
* JavaScript (ES Modules)
* [Three.js](https://threejs.org/) (for WebGL rendering)
* [Three.js OrbitControls](https://threejs.org/docs/#examples/en/controls/OrbitControls) (for panning/zooming)
* [Font Awesome](https://fontawesome.com/) (for icons)
* [Google Fonts](https://fonts.google.com/) (Jost font for text)

## Files

* `adhd-skill-tree.htm`: The main interactive skill tree visualization file.
* `adhd-skill-tree-explanation.htm`: Contains detailed explanations for each skill/trait, linked from the main visualization.

## How to Use / Run

1.  Clone or download this repository.
2.  Ensure both `adhd-skill-tree.htm` and `adhd-skill-tree-explanation.htm` are in the same directory.
3.  Open the `adhd-skill-tree.htm` file in a modern web browser (like Chrome, Firefox, Edge, Safari) that supports ES Modules and WebGL.
4.  Interact:
    * **Pan:** Click and drag the mouse.
    * **Zoom:** Use the mouse scroll wheel or pinch gesture on touch devices.
    * **View Details:** Hover over a skill icon to see its tooltip.
    * **Learn More:** Click a skill icon to open its explanation in a new tab (requires `adhd-skill-tree-explanation.htm` to be present).
    * **Toggle Theme:** Use the button in the bottom-right corner.

## Content Source

The descriptions, categories, and concepts for the ADHD skills, traits, and strategies presented in this visualization are based on user-provided information. This information generally aligns with common knowledge regarding ADHD management but should not be considered exhaustive or clinical advice.

## Customization

The content of the skill tree (skills, descriptions, connections, icons, links, layout) is primarily defined within the `skillsData` array inside the `<script type="module">` block in `adhd-skill-tree.htm`. You can modify this data structure to customize the tree.
