# 📝 How to Add a Blog Post (HBS RCS Quarto Blog)

The below instructions assume that the poster is using GitHub Desktop and RStudio.

## 1. Get the code

### 1a. If posting for the first time, clone the GitHub repo:

1.  Open **GitHub Desktop**
2.  Click **File → Clone Repository**
3.  Choose `hbs-rcs/rcs-blog`
4.  Select a local folder and click **Clone**

### 1b. If you've posted before, fetch the current main branch:

1.  Open **GitHub Desktop**
2.  Select the `rcs-blog` repo and make sure that the `main` branch is selected
3.  Click **Fetch origin** at the top of the window
3.  If commits exist on the main branch that are not on your local copy, click **Pull origin**

------------------------------------------------------------------------

## 2. Create a new branch

1.  At the top of the GitHub Desktop window, click **Current Branch** and make sure that `main` is selected
2.  Click **New Branch**
3.  Name it something descriptive like:
        `blog-post-title`
4.  Click **Create Branch**
5.  Select your new branch and publish it to the repo

------------------------------------------------------------------------

## 3. Create your post

1.  Open the rcs-blog repo in RStudio
2.  Go to the `posts` folder
3.  Create a new folder with a descriptive name for your post (e.g. `2026-04-07_blog-post-title`), either manually or by copying a previous post
4.  Create a file called `index.qmd` (or open `index.qmd` if you copied a folder)

------------------------------------------------------------------------

## 4. Add post metadata

At the top of `index.qmd` include metadata such as the following:

``` yaml
---
title: "Your Post Title"
author: "Your Name, Co-Author's Name where applicable"
date: "2026-04-07"
description: "Optional short summary of the post"
categories: [methods, Python, large language models, other relevant topics for tagging]
image: "optional-featured-image.jpg"
---
```

------------------------------------------------------------------------

## 5. Write your post

-   Write in Markdown + code chunks (R, Python, Stata, etc.)
-   Add images to the same folder and reference them like:

    ``` markdown
    ![](image.png)
    ```

------------------------------------------------------------------------

## 6. Preview locally

-   In RStudio: click **Render**
-   Or run:
    ``` bash
    quarto preview
    ```

Check that: 
-  The post shows up on the homepage 
-  Formatting looks
right 
-  Code runs (if applicable)

------------------------------------------------------------------------

## 7. (If using code) Freeze results

Add to YAML at the top with the rest of the metadata:

``` yaml
execute:
  freeze: true
```

Then render once. This saves outputs so others don't need your setup.

------------------------------------------------------------------------

## 8. Commit and push

1.  Go back to GitHub Desktop
2.  You'll see your changed files listed
3.  Add a commit message (e.g., "Add blog post: Blog Post Title")
4.  Click **Commit to `blog-post-title`** (where `blog-post-title` is the name of the branch you created earlier)
5.  Click **Push origin**

------------------------------------------------------------------------

## 9. Open a pull request

1.  After pushing, click **Create Pull Request**; this will open GitHub in your browser
2.  Optionally add a short description for the pull request
3.  Click **Create Pull Request**
4.  If you would like any team member(s) to review, click the gear icon next to "Reviewers" on the right and select them; they will be notified of the request and will be able to review and make comments
5.  When ready to publish, click **Merge pull request** and **Confirm merge**
6.  Delete your branch using the button 

------------------------------------------------------------------------

## 10. After merge

Once your pull request is merged, the site updates automatically and your post will appear on the blog within ten to fifteen minutes 🎉

------------------------------------------------------------------------

## Tips

-   Use `draft: true` in YAML if your post isn't ready yet
-   Keep folder names lowercase with hyphens
-   Put all images inside your post folder

------------------------------------------------------------------------

## Optional: Simple Post Template

You can copy this into a new `index.qmd`:

```` markdown
---
title: "Post Title"
author: "Your Name"
date: "2026-04-07"
description: "Short summary"
categories: [R]
image: "image-file.jpg"
execute:
  freeze: true
---

## Introduction

Write your intro here.

## Example

```{r}
summary(cars)
```
````
