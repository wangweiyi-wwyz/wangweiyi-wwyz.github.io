# Personal Portfolio Website

Welcome to the source code of my personal portfolio website. This project is built using a modern static site generation stack, focusing on speed, responsiveness, and automated deployment.

## 🚀 Tech Stack

* **Framework:** [Hugo](https://gohugo.io/) (Fast and flexible Static Site Generator)
* **Styling:** [Tailwind CSS](https://tailwindcss.com/) (Utility-first CSS framework)
* **Theme:** [Aafu](https://github.com/aafu-theme) (Integrated as a Git submodule)
* **CI/CD:** GitHub Actions (Automated build and deployment)
* **Hosting:** GitHub Pages

## 📁 Project Structure

Here is a brief overview of the core directories and files in this repository:

* `.github/workflows/`: Contains the CI/CD pipeline configuration (`hugo.yaml`) for automatic deployment to GitHub Pages.
* `content/`: The actual Markdown files containing the posts, pages, and portfolio content.
* `assets/` & `static/`: Directories containing images, custom CSS/JS, and other static resources.
* `themes/aafu/`: The Hugo theme utilized for this site, managed as a Git submodule.
* `tailwind.config.js`: Configuration file for customizing Tailwind CSS utility classes.
* `config.yaml`: The main configuration file for the Hugo site settings.
* `package.json`: Manages the Node.js dependencies (primarily for Tailwind CSS processing).

## 🛠️ Local Development

To run this project locally on your machine, follow these steps:

### Prerequisites

1.  **Hugo (Extended Version):** You must install the *Extended* version of Hugo to process Tailwind CSS. Verify your installation by running `hugo version` (it should mention "extended").
2.  **Node.js & npm:** Required for installing styling dependencies.
3.  **Git:** For cloning the repository and its submodules.

### Setup Instructions

1.  **Clone the repository:**
    Because the theme is added as a submodule, you must include the `--recursive` flag when cloning.
    ```bash
    git clone --recursive [https://github.com/wangweiyi-wwyz/](https://github.com/wangweiyi-wwyz/)<your-repo-name>.git
    cd <your-repo-name>
    ```
    *(If you already cloned it without the flag, run: `git submodule update --init --recursive`)*

2.  **Install Node dependencies:**
    This will install Tailwind CSS and related PostCSS plugins defined in `package.json`.
    ```bash
    npm install
    ```

3.  **Run the local development server:**
    Start the Hugo server with drafts enabled.
    ```bash
    hugo server -D
    ```

4.  **Preview:**
    Open your browser and navigate to `http://localhost:1313`. The server supports live-reloading, so changes to your files will reflect instantly.

## ☁️ Deployment

This project utilizes **GitHub Actions** for continuous integration and deployment. 

Any changes pushed to the `main` branch will automatically trigger the workflow defined in `.github/workflows/hugo.yaml`. The workflow will install dependencies, build the static site, and deploy the `public/` directory directly to GitHub Pages. No manual build process is required!

## 📝 License

[MIT License]
