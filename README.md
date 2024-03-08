# Hosting a Resume using GitHub Pages and Jekyll

## Purpose

This is a step-by-step guide on how to host your resume on a website using GitHub Pages and Jekyll.

This guide heavily follows the principles from Andrew Etter's book _Modern Technical Writing_ as outlined in the next section.

## Principles in Modern Technical Writing

Andrew Etter discusses several principles to writing good software documentation in his book, _Modern Technical Writing_. Notably:

* **Use a lightweight markup language to write documentation**. We use lightweight markup languages like Markdown because they are compatible with various different platforms, free to use, human-readable, and straightforward to learn.

* **Use a static site generator to host your documentation**. Static sites are fast, simple, secure, and portable because they do not require databases nor servers to function. With static site generators like Jekyll, all we need is a lightweight markup language document to create and easily customize our static sites. Therefore, we can make a beautiful and functional documentation website with ease.

* **Use a distributed version control system (DVCS) to share/host documents**. Using a DVCS like GitHub makes it easy to upload files into a repository and share it with others. In addition, it keeps track of any changes to the documents so we can collaborate without worry. 

We apply these principles by hosting a Markdown resume using a lightweight static site generator Jekyll and a DVCS GitHub/GitHub Pages.


## Prerequisites

* A GitHub account. Sign-up [here](https://github.com/) to create an account for free.

* A Markdown file containing your resume saved as `index.md`. For guidance on how to write in markdown look at [Markdown Tutorial](https://www.markdowntutorial.com/).

* Learn about what Git and GitHub is. For more information, refer to [What is Git and GitHub](https://www.coursera.org/articles/what-is-git) and [GitHub Tutorial](https://docs.github.com/en/get-started/start-your-journey/hello-world).


## Instructions


### Creating a Repository

1. Log into your GitHub account.
2. Click **+** icon on the top right corner of the page.
3. Click **New repository** option that appears.

   ![](https://github.com/gapy04/gapy04.github.io/blob/main/images/new_repo.png)

4. Type `[your_github_username].github.io` in the repository name box (i.e. hippo.github.io).

   ![](https://github.com/gapy04/gapy04.github.io/blob/main/images/repo_name.png)

5. Enter a short description that describes the repository.
6. Select **Public** option for your repository.
7. Select **Initialize this repository with a README file** option. 
8. Select **MIT License** option under **Choose a License**.
9. Click the **Create repository** button at the very bottom. 

You now have a repository where all your files can be uploaded and shared.


### Setting up GitHub Pages

1. Go to your repository.
2. Click **Settings** under your repository name.

   ![](https://github.com/gapy04/gapy04.github.io/blob/main/images/settings.png)

3. Click **Pages** on the left sidebar under the Code and automation section.

   ![](https://github.com/gapy04/gapy04.github.io/blob/main/images/pages.png)

4. Select **Deploy from a branch** under source in the Build and deployment section.
5. Select **main** in the first dropdown under the branch subsection.
6. Select **/ (root)** in the second dropdown under the branch subsection.

   ![](https://github.com/gapy04/gapy04.github.io/blob/main/images/github_pages_settings.png)

7. Click **save** if applicable under the branch subsection.
8. Open a new tab in your browser.
9. Type `https://[your_github_username].github.io/` (i.e. https://hippo.github.io/) in the address bar.
10. Press **Enter** on your keyboard.

You now have a simple static website! At this point, you will see your README on your website. Next, we will host our resume.


### Hosting your Resume

1. Go back to your GitHub repository.
2. Click **Add file** beside the green code button.
3. Click **Upload files** option on the menu that appears.

   ![](https://github.com/gapy04/gapy04.github.io/blob/main/images/upload_files.png)

4. Click **Choose your files**.

   ![](https://github.com/gapy04/gapy04.github.io/blob/main/images/choose_files.png)

5. Select your resume that is saved as `index.md`.
6. Write a commit message under **Commit changes**. This should be a message about what we are doing such as "Add files via upload."
7. Select **Commit directly to the main branch** option.
8. Click **Commit changes** at the bottom. You will be redirected back to your repository's main page.

   ![](https://github.com/gapy04/gapy04.github.io/blob/main/images/commit_changes.png)

9. Click **Actions** tab under your repository name.

   ![](https://github.com/gapy04/gapy04.github.io/blob/main/images/actions.png)

10. Check if all the items under **All workflows** have a green checkmark. If there is an orange dot beside an item, this means your changes are still being uploaded on your website.

   ![](https://github.com/gapy04/gapy04.github.io/blob/main/images/workflows.png)

11. Go to your website at `https://[your_github_username].github.io/`.
12. Check your website content has been updated with your resume.

You have now hosted your resume! Next, we will customize our website. 


### Adding a Theme to your Website using Jekyll

There are several GitHub supported themes we can choose from [here](https://pages.github.com/themes/).

GitHub also allows us to use any other theme if it is already hosted on a GitHub repository. For example, [Beautiful Jekyll](https://github.com/daattali/beautiful-jekyll) by user [@daattali](https://github.com/daattali).

1. Pick a theme you want to use either from GitHub supported themes or any other Jekyll themes already hosted on GitHub.
2. Go back to your GitHub repository.
3. Click **Add file** beside the green code button.
4. Click **Create new file** option on the menu that appears.

   ![](https://github.com/gapy04/gapy04.github.io/blob/main/images/create_file.png)

5. Type `_config.yml` in the **Name your file...** box.

   ![](https://github.com/gapy04/gapy04.github.io/blob/main/images/config_name.png)

6. Add a new line in the file for the theme name.
    * If you are using a GitHub supported theme, type `theme: jekyll-theme-[theme_name]` replacing [theme_name] with name of the theme (i.e. theme: jekyll-theme-cayman).
    * If you are using any other themes hosted on GitHub, type `remote_theme: [theme_name]` replacing [theme_name] with name of the theme (i.e. remote_theme: beautiful-jekyll).
    * Note: Only one `theme: jekyll-theme-[theme_name]` or `remote_theme: [theme_name]` is allowed.
7. (Optional) Add metadata lines accepted by your theme on a new line. You can identify these by reading the README on your theme's repository. Examples include:
    * `title: [website_title]` (i.e. title: My Resume)
    * `description: [website_description]` (i.e. description: Welcome to my website!)

   ![](https://github.com/gapy04/gapy04.github.io/blob/main/images/config_content.png)

8. Click green **Commit changes** button on the right.
9. Write a commit message in the pop-up.
10. Click **Commit changes** again in the pop-up.
11. Check the workflow under the **Actions** tab is all green.
12. Go to your website `https://[your_github_username].github.io/`.
13. Check your website content has been updated with your selected theme.

Your repository should look something like this:

![](https://github.com/gapy04/gapy04.github.io/blob/main/images/resume.gif)

Congratulations! You have successfully hosted your resume on a static website with customizations!

## More Resources

Here are some other additional guides and resources to help you. 

* [Markdown Tutorial](https://www.markdowntutorial.com/)
* [Markdown Guide](https://www.markdownguide.org/getting-started/)
* [Introduction to Git and GitHub](https://www.coursera.org/articles/what-is-git)
* [GitHub Tutorial](https://docs.github.com/en/get-started/start-your-journey/hello-world)
* [GitHub Supported Themes List](https://pages.github.com/themes/)
* [Beautiful Jekyll](https://github.com/daattali/beautiful-jekyll)
* [How to host your website locally with Jekyll](https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/testing-your-github-pages-site-locally-with-jekyll)
* [Troubleshooting 404 errors for GitHub Pages sites](https://docs.github.com/en/pages/getting-started-with-github-pages/troubleshooting-404-errors-for-github-pages-sites)
* [Troubleshooting Jekyll build errors for GitHub Pages site](https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/troubleshooting-jekyll-build-errors-for-github-pages-sites)

## Authors

- Agape Seo, [@gapy04](https://www.github.com/gapy04)

## Acknowledgements

- Aivee Teodocio, [@aivee-teodocio](https://github.com/aivee-teodocio) - Reviewed this guide.
- Eseosa Ataga, [@Marie-Lenora](https://github.com/Marie-Lenora) - Reviewed this guide.
- [@pages-theme](https://github.com/pages-themes) - Provided [Cayman](https://github.com/pages-themes/cayman) Jekyll theme template.
- [Andrew Etter's book Modern Technical Writing](https://www.amazon.ca/Modern-Technical-Writing-Introduction-Documentation-ebook/dp/B01A2QL9SS)
- [How to write a good README](https://bulldogjob.com/news/449-how-to-write-a-good-readme-for-your-github-project)

## FAQ

### **Why should we use GitHub Pages for our website?**

GitHub is a popular and widely used platform to upload and share files. GitHub Pages provides a seamless connection to GitHub repositories with Jekyll, hence making it easier to create a website. Additionally, we can host a website for free while also maintaining version control on GitHub. Hence, we use GitHub Pages for our website.

### **Why is my website giving me an error?**
Check your repository name is `[your_github_username].github.io` and you are going to `https://[you_github_username].github.io/`.

For further troubleshooting, go to [Troubleshooting 404 errors for GitHub Pages sites](https://docs.github.com/en/pages/getting-started-with-github-pages/troubleshooting-404-errors-for-github-pages-sites).
