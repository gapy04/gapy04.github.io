
# Hosting a Resume using GitHub Pages and Jekyll

This is a step-by-step guide on how to host your resume on a website using GitHub Pages and Jekyll for beginners.

This guide heavily follows the principles from Andrew Etter's book _Modern Technical Writing_ as outlined in the next section.

## Principles in Modern Technical Writing

Andrew Etter discusses several principles to writing good software documentation in his book, _Modern Technical Writing_.

Some of the his key principles are:

* **Use a lightweight markup language like Markdown to write documentation**. We use lightweight markup languages because they are compatible with various different platforms, free to use, human-readable, and straightforward to learn. This allows us to collaborate with various groups of people.

* **Use a static site generator like Jekyll to host your documentation**. Static sites are fast, simple, secure, and portable. They do not require databases nor servers to function. All you need is a lightweight markup language document and you are done! Tools such as Jekyll also allows us to easily customize our websites to our own tastes. Therefore, we can make a beautiful and functional documentation website with ease.

* **Use a distributed version control system (DVCS) like GitHub to share/host documents**. Using a DVCS like GitHub makes it easy to upload files into a repository and share it with others. It also allows us to collaborate with other people, work offline and keep track of any changes to the documents. 

We now apply these principles by hosting a resume written in Markdown on a lightweight static website using GitHub Pages and Jekyll.


## Prerequisites

* A GitHub account. Sign-up [here](https://github.com/) to create an account for free.

* A Markdown file containing your resume saved as `index.md`. For guidance on how to write in markdown look at [Markdown Tutorial](https://www.markdowntutorial.com/).


## Instructions


### Creating a Repository

1. Log into your GitHub account.
2. Click **+** icon on your top right corner of the page.
3. Click **New repository** option on the menu that appears.
![](https://github.com/gapy04/gapy04.github.io/blob/main/images/new_repo.png)
4. Type `[your_github_username].github.io` in the repository name box (i.e. hippo.github.io).
![](https://github.com/gapy04/gapy04.github.io/blob/main/images/repo_name.png)
5. Enter a short description that describes the repository.
6. Select **Public** option for your repository.
7. Select **Initialize this repository with a README file** option. 
8. Select **MIT License** option under **Choose a License**
9. Click the **Create repository** button at the very bottom. 

You have now created a repository where all your files can be uploaded and shared.


### Setting up GitHub Pages

1. Go to your repository. Note: If you just created your repository, you should already be in it.
2. Click **Settings** under your repository name.
![](https://github.com/gapy04/gapy04.github.io/blob/main/images/settings.png)
3. Click **Pages** on the left sidebar under the Code and automation section. ![](https://github.com/gapy04/gapy04.github.io/blob/main/images/pages.png)
4. Select **Deploy from a branch** under source in the Build and deployment section.
5. Select **main** in the first dropdown under the branch subsection.
6. Select **/ (root)** in the second dropdown under the branch subsection.
![](https://github.com/gapy04/gapy04.github.io/blob/main/images/github_pages_settings.png)
7. Click **save** if applicable under the branch subsection.
8. Open a new tab in your browser.
9. Type `https://[your_github_username].github.io/` (i.e. https://hippo.github.io/) in the address bar of your new browser.
10. Press **Enter** on your keyboard.

You have now created a simple static website! At this point, you will see your README contents on your website. Next, we will host our resume on the website.


### Hosting your Resume

1. Go back to the settings tab in your browser. 
2. Click on your repository name at the top to go back to your GitHub repository.
3. Click **Add file** beside the green code button.
4. Click **Upload files** option on the menu that appears.
![](https://github.com/gapy04/gapy04.github.io/blob/main/images/upload_files.png)
5. Click **Choose your files**.
![](https://github.com/gapy04/gapy04.github.io/blob/main/images/choose_files.png)
6. Select your resume that is saved as `index.md`.
7. Write a commit message under **Commit changes**. This can be anything about the action we are about to do such as "Add files via upload."
8. Select **Commit directly to the main branch** option.
9. Click **Commit changes** at the bottom. You will be redirected back to your repository's main page.
![](https://github.com/gapy04/gapy04.github.io/blob/main/images/commit_changes.png)
10. Click **Actions** tab under your repository name.
![](https://github.com/gapy04/gapy04.github.io/blob/main/images/actions.png)
11. Check if all the items under **All workflows** have a green checkmark. If there is an orange dot beside an item, this means your changes are still being uploaded on your website.
![](https://github.com/gapy04/gapy04.github.io/blob/main/images/workflows.png)
12. Go to your website at `https://[your_github_username].github.io/`
13. Check your website content has been updated with your resume.

You have now hosted your resume! Next, we will add some customization to our website. 


### Adding a Theme to your Website using Jekyll

There are several GitHub supported themes we can choose from [here](https://pages.github.com/themes/).

GitHub also allows us to use any other theme as long as it is already hosted on a GitHub repository. For example, [Beautiful Jekyll](https://github.com/daattali/beautiful-jekyll) by user [@daattali](https://github.com/daattali)

1. Pick a theme you want to use either from GitHub supported themes or any other Jekyll themes already hosted on GitHub.
2. Go back to your GitHub repository.
3. Click **Add file** beside the green code button.
4. Click **Create new file** option on the menu that appears.
![](https://github.com/gapy04/gapy04.github.io/blob/main/images/create_file.png)
5. Type `_config.yml` in the **Name your file...** box.
![](https://github.com/gapy04/gapy04.github.io/blob/main/images/config_name.png)
6. Add a new line in the file for the theme name.
    * If you are using a GitHub supported theme, type `theme: jekyll-theme-[theme_name]` replacing [theme_name] with name of the theme (i.e. theme: jekyll-theme-cayman).
    * If you are using any other themes hosted on GitHub, type `remote_theme: [theme_name]` replacing [theme_name] with name of the theme found in the README (i.e. remote_theme: beautiful-jekyll).
7. Press **Enter** on your keyboard to go to a new line
8. (Optional) Add metadata lines accepted by your theme. Note: you can identify these by reading the README on your theme's repository. Examples include:
    * `title: [website_title]` (i.e. title: My Resume)
    * `description: [website_description]` (i.e. description: Welcome to my website!)
![](https://github.com/gapy04/gapy04.github.io/blob/main/images/config_content.png)
8. Click green **Commit changes** button on the right side.
8. Write a commit message in the pop-up.
9. Click **Commit changes** again in the pop-up.
10. Check until the workflow under actions tab is all green.
11. Go to your website at `https://[your_github_username].github.io/`
12. Check your website content has been updated with your selected theme.

Note: Only one `theme: jekyll-theme-[theme_name]` or `remote_theme: [theme_name]` is allowed.

Congratulations! You have successfully hosted your resume on a static website with customizations!

## More Resources

Here are some other additional guides and resources to help you. 

* [Markdown Tutorial](https://www.markdowntutorial.com/)
* [Markdown Guide](https://www.markdownguide.org/getting-started/)
* [GitHub Supported Themes List](https://pages.github.com/themes/)
* [Beautiful Jekyll](https://github.com/daattali/beautiful-jekyll)
* [How to host your website locally with Jekyll](https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/testing-your-github-pages-site-locally-with-jekyll)
* [Troubleshooting 404 errors for GitHub Pages sites](https://docs.github.com/en/pages/getting-started-with-github-pages/troubleshooting-404-errors-for-github-pages-sites)
* [Troubleshooting Jekyll build errors for GitHub Pages site](https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/troubleshooting-jekyll-build-errors-for-github-pages-sites)

## Authors

- Agape Seo, [@gapy04](https://www.github.com/gapy04)

## Acknowledgements

- Aivee Teodocio, [@aivee-teodocio](https://github.com/aivee-teodocio) - Helped review this guide.
- Eseosa Ataga, [@Marie-Lenora](https://github.com/Marie-Lenora) - Helped review this guide.
- [@pages-theme](https://github.com/pages-themes) - provided Cayman Jekyll theme template
- [Andrew Etter's book Modern Technical Writing](https://www.amazon.ca/Modern-Technical-Writing-Introduction-Documentation-ebook/dp/B01A2QL9SS)
- [How to write a Good readme](https://bulldogjob.com/news/449-how-to-write-a-good-readme-for-your-github-project)

## FAQ

#### **Why should we use GitHub Pages for our website?**

We use GitHub Pages to host our website because it is simple and easy to use. Additionally, it is one of the resources where we can host a website for free while also maintaining version control.

#### **Why is my resume not showing up on my website?**

Check your resume file is saved as `index.md`. GitHub Pages looks for files named `index.md`, `index.html` or `README.md` as the primary file to display on your website. Note: GitHub Pages will choose a `index.md` over `README.md` if both are present.

#### **Why is my website giving me an error?**
Check your repository name is `[your_github_username].github.io` (i.e. hippo.github.io).

For further troubleshooting, go to [Troubleshooting 404 errors for GitHub Pages sites](https://docs.github.com/en/pages/getting-started-with-github-pages/troubleshooting-404-errors-for-github-pages-sites).

#### **Why is the theme not updating on my website?**

Check your `_config.yml` file has the correct theme name.
* For [GitHub supported themes](https://pages.github.com/themes/), use `theme: jekyll-theme-[theme_name]` (i.e. theme: jekyll-theme-cayman).

* For any other GitHub hosted themes, use `remote-theme: [theme_name]` (i.e. remote-theme: beautiful-jekyll)

If you used `remote-theme` for a GitHub hosted themes but it does not work, the owner may have not enabled it. In this case, you will need to find a new theme.

For further troubleshooting, go to [Troubleshooting Jekyll build errors for GitHub Pages site](https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/troubleshooting-jekyll-build-errors-for-github-pages-sites).
