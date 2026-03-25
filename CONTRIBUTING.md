# Contributing to XPM Registry 🧬

First of all, thank you for showing interest in contributing to the **X-Phage Ecosystem**. Your contributions help expand the boundaries of high-performance computing and neural-integrated software.

To maintain the stability and security of the **Titan Core (v3.5.0)**, we enforce a strict automated distribution model. Please follow this guide to get your library published.

---

## 🛠 Submission Checklist

Before you start, ensure your package adheres to the **X-Phage Standard (XPS-1)**:

- [ ] **File Format:** Library must be a single standalone `.xh` header.

- [ ] **Naming:** Package names must be lowercase, alphanumeric, and use hyphens (e.g., `neural-net-v2`).

- [ ] **Integrity:** Every release MUST have a corresponding `.sha256` checksum.

- [ ] **Licensing:** Include a license header at the top of your `.xh` file (MIT, Apache 2.0, and BSD are preferred).

---

## 🚀 The Publishing Workflow

### 1. Host Your Release (GitHub)
XPM does not store code directly; it acts as a decentralized proxy. You must host your code on your own GitHub repository.

1.  Create a **GitHub Release** in your repository.

2.  **Tagging:** You MUST use the format `package_name@version`.
    * *Example:* `matrix-math@1.0.0`

3.  **Upload Assets:** Attach the following two files to the release assets:
    * `your_package.xh`
    * `your_package.sha256`

> **Pro Tip:** Generate a checksum quickly via terminal:
> `sha256sum your_package.xh > your_package.sha256`

### 2. Register Your Package
To make your package "discoverable" by the `xphage install` command, you need to update our central index.

1.  **Fork** this repository (`xpm-registry`).
2.  Open `index.json` and append your package metadata:
```json
"your-package-name": {
  "owner": "your-github-username",
  "description": "A high-level description of your module's purpose.",
  "latest": "1.0.0",
  "versions": ["1.0.0"]
}
```


**3. Submit a Pull Request to the main branch.**

## ⚖️ Review Process

**Once your PR is submitted, our CI/CD pipeline and maintainers will verify:**

1.**Checksum Accuracy**: We verify if the .sha256 asset matches the .xh file.

2.**Namespace Safety**: Ensure your package name doesn't conflict with stdlib or existing high-profile packages.

3.**Syntax Check**: The .xh file must be valid X-Phage syntax (checked via xphage --check).


## 💬 Community & Support

1.**If you encounter issues during the submission process, feel free to:**

2.**Open an Issue on this repository.**

3.**Reach out via the AeonCoreX Developer Forum.**

### Thank you for building the future with X-Phage!

***(C) 2026 AeonCoreX Lab. All Rights Reserved.***
