## README: FTT Public Site Infrastructure

### Project Context: Fish Tank Tech (FTT)

This repository hosts the static assets, configuration, and source files necessary to build and host the Fish Tank Tech (FTT) public-facing website.

In line with the FTT core philosophy, this site is treated as **infrastructure**, not a product. The design prioritizes **legibility**, **durability**, and a minimal, archival aesthetic.

---

### Purpose and Explicit Constraints

The primary function of this repository is to serve as a **clear, durable pipeline** for disseminating FTT's core context, philosophy, and technical documentation.

#### **Core Goals**

1.  **Legibility over Decoration:** Ensure all content is highly scannable and accessible.
2.  **Durability:** Minimize dependencies and complexity to ensure the site remains operational and understandable for the long term.
3.  **Inspectability:** The entire structure should be navigable and explainable to a competent non-developer.

#### **Explicit Constraints (Why this is simple)**

This repository is strictly a container for static content and deployment configuration.

* **No Hidden Logic:** There is no server-side processing, database connection, or complex runtime environment involved.
* **Static Output:** The site generates clean, pre-built files (HTML, CSS) to reduce hosting complexity and potential failure modes.
* **Minimal Tooling:** Build and deployment processes are kept deliberately simple and are documented explicitly (see the `config` folder).

---

### Repository Structure

Understanding the layout is crucial for maintenance. This structure is designed to separate content from presentation and configuration, favoring a clear hierarchy.

| Directory | Content Purpose | FTT Alignment |
| :--- | :--- | :--- |
| `/content/` | Site source files (Markdown, images, etc.) | Holds the core narrative and documentation. **Editable Inputs.** |
| `/layouts/` | HTML templates and structure | Defines the minimalist presentation and content hierarchy. |
| `/static/` | Static assets (CSS, low-level scripts) | Contains styling focused on function and legibility. |
| `/config/` | Build configuration and settings | Defines **explicit constraints** and build parameters. |

---

### Maintenance and Modification

Future modifications must align with the FTT principles: clarity, low dependency, and durability. We seek progressive clarity, not complex perfection.

#### **Contribution Guide**

| Task | Action | Principle Supported |
| :--- | :--- | :--- |
| **Update Text/Data** | Edit Markdown files within `/content/`. | **Inputs must be editable and inspectable.** |
| **Change Styling** | Modify CSS within `/static/` or templates in `/layouts/`. | **Favor clarity over cleverness** and decoration. |
| **Add New Dependency** | **AVOID.** If unavoidable, document its specific tradeoff, maintainer, and potential failure modes in a dedicated `DEPENDENCY_NOTES.md` file. | **Minimize unnecessary dependencies.** |

> **Note on Assumptions:** Assume that any change made here will need to be understood and maintained by someone who did not originally write it. Favor consistent, plainspoken code over clever optimizations.
