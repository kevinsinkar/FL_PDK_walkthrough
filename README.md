# FlexLogger Plug-In Development Guide

An interactive, single-page walkthrough for building FlexLogger plug-ins — from choosing the right template to deploying and testing your first plug-in.

**[View the live guide →](https://kevinsinkar.github.io/FL_PDK_walkthrough/)**

> **Disclaimer:** This is **not** an official document of National Instruments (NI) or Emerson. This is an independent side project created to help FlexLogger users build plug-ins using the Plug-In Development Kit (PDK). All product names, logos, and brands referenced are property of their respective owners. For official documentation, refer to the [NI FlexLogger documentation](https://www.ni.com/docs/en-US/bundle/flexlogger/page/flexlogger-manual-overview.html).

---

## What This Is

A self-contained HTML reference guide designed for LabVIEW developers and test engineers who are new to FlexLogger plug-in development. It covers the full development workflow across six sections, with a guided walkthrough feature that filters the entire guide down to just what matters for your chosen template.

## Features

### Reference Guide (6 Tabs)
- **Choose Your Template** — Side-by-side comparison of Producer, Calculator, Consumer, and Command templates with a decision matrix table
- **Plug-In Lifecycle** — Visual state machine showing Initialize → Configure → Process → Cleanup → Finalize
- **LabVIEW ↔ Plug-In Mapping** — How standard LabVIEW patterns map to the FlexLogger plug-in structure
- **Step-by-Step Build** — Install → Create → Customize → Test → Deploy workflow
- **VI Toolbox Reference** — Every VI in the FlexLogger palette with usage context and gotchas
- **Pitfalls & Best Practices** — Common mistakes sourced from the NI R&D team and official docs

### Interactive Walkthrough
- **Click any template card** (or any row in the decision matrix) to launch a guided, template-specific walkthrough
- **Checklist tracking** — Each step has concrete checkbox items so you can track progress as you build
- **Progress bar** — Visual step-by-step indicator with completion percentages
- **Inline pitfall warnings** — Relevant gotchas surface at the exact step where they'd bite you, not in a separate tab
- **Contextual VI references** — Only the VIs relevant to your current step are shown
- **Copy Checklist** — Export your walkthrough as formatted plain text to paste into a ticket, wiki, or notepad

## Usage

This is a single HTML file with no dependencies, no build step, and no framework. Just open it in a browser or host it on GitHub Pages.

### GitHub Pages

1. Push `index.html` (or the HTML file renamed to `index.html`) to a repo
2. Go to **Settings → Pages → Source** and select your branch
3. The guide will be live at `https://your-username.github.io/your-repo-name/`

### Local

Open the HTML file directly in any modern browser. Everything is self-contained — styles, scripts, and content are all inline.

## Who This Is For

- **LabVIEW developers** building their first FlexLogger plug-in
- **Test engineers** evaluating which plug-in template fits their hardware integration
- **Teams** onboarding new members to FlexLogger plug-in development

## Tech

- Single-file HTML/CSS/JS — no build tools, no npm, no dependencies
- Fonts loaded from Google Fonts (DM Sans + DM Mono)
- Accessible tab navigation with full keyboard support (arrow keys, Home/End, Escape)
- ARIA roles and labels throughout
- Responsive layout for tablets and smaller screens

## Contributing

If you spot an error, have a suggestion, or want to add coverage for a scenario not yet included, feel free to open an issue or submit a pull request.

## License

This project is provided as-is for educational purposes. It is not affiliated with, endorsed by, or supported by National Instruments, Emerson, or any of their subsidiaries. Use at your own discretion.