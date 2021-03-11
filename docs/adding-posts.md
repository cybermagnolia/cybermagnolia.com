# Adding Blog Posts

We'd like every member of CyberMagnolia's core team and community to be able to contribute articles to the [website](https://cybermagnolia.com/). If you're here to add a blog post, here's some love for you: :heart:

Here's a guide to help you do it. If you have any difficulties, please reach out to [Daria](https://twitter.com/DariaGrudzien) who will be happy to help you.

> Note: this guide will work for Mac & Linux users, but it needs to be proofed by a Windows user.

## Prerequisites

* Basic knowledge of [git](https://www.git-tower.com/blog/git-cheat-sheet/) & [Markdown](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)
* A GitHub account & access to this repository (please ping Daria on CyberMagnolia Slack to get it)
* Ability to use command line
* This repository cloned on your computer
* Initialized submodule with the blog theme
* (Optionally) Having [Hugo](https://gohugo.io/getting-started/installing/) installed

Here are the commands to clone the repo and initialize the submodule:

    ```sh
        git clone git@github.com:cybermagnolia/cybermagnolia.com.git
        cd <your cybermagnolia.com project directory>
        git submodule init
    ```

## Adding Posts

There are two ways to add the blog post:

* By creating the file [manually](#adding-posts-by-manually-creating-files)
* By creating the file [with Hugo](#creating-new-blog-post-with-hugo) and previewing it locally

### Adding Posts By Manually Creating Files

Start by creating your own git branch, see first step of[#Creating-The-Pull-Request-And-Deploying-Your-Post]

1. Go to the `content/blog/` directory:

    ```sh
        cd <your cybermagnolia.com project directory>
        cd content/blog/
    ```

2. Create a new markdown file in the blog directory - it's title will become the URL of the blog post so use dashes to separate words (e.g. `jane-smith-interview.md`)

    ```sh
        touch jane-smith-interview.md
    ```

3. Copy the headers from another post in the same directory (i.e. everything at the top of the post including `+++` section markers)

    ```md
        +++
        title = "Online Happy Hours December 2020"
        description = "Join us for our next friendly & informal online chat"
        author = "Daria Grudzien"
        date = "2020-11-25"
        tags = ["happy_hours", "meetup"]
        [[images]]
        src = "/img/happyhours_post.png"
        alt = "Photo"
        stretch = "stretchH"
        +++
    ```

4. Update all relevant fields: `title`, `description`, `author`, `date`, `tags`

5. To update the image source (`src` from the previous example), upload the post cover photo of your choice into `static/img/` directory with some meaningful name, e.g. `jane_smith_interview.jpg`.

    * You will find  image templates in the `design_assets` directory in our CyberMagnolia Google Drive folder. To get access, please request it in the `#organizers` channel on our Slack.

    * Prefer a `.jpeg` or `.jpg` file over `.png` - it's smaller and will make our website faster.

    * The simplest method of adding the image is moving the file into the folder. You can open it from your command line. This example assumes that you are in the root directory of the `cybermagnolia.com` directory:

    ```sh
        open static/img/
    ```

    This will open the directory with the images, and you can drag & drop your image there.

6. Update `src` in your blog post header with the name of the file you've just added while keeping the `/img/` directory:

    ```md
        [[images]]
        src = "/img/jane_smith_interview.jpg"
    ```

## Creating New Blog Post With Hugo

TODO

## Creating The Pull Request And Deploying Your Post :desktop:

There are few common conventions that make cooperating on a repository easier. Here are the things to keep in mind when creating the pull request:

1. Make sure to create your own branch with your name prefix in it, like in this example:

```sh
    git checkout -b daria/add-jane-smith-interview
```

2. When commiting the changes, add a meaningful message following the [commitizen](https://raw.githubusercontent.com/commitizen/cz-cli/master/meta/screenshots/add-commit.png) standard, like in this exmaple:

```sh
    git add .
    git commit -m "feat: add jane smith interview"
```
If you can't figure out the message format, just go with your gut — it's more important that you commit stuff than get stuck on naming commits.

3. Push your branch to GitHub:

```sh
    git push -u origin daria/add-jane-smith-interview
```

4. Go to [GitHub](https://github.com/cybermagnolia/cybermagnolia.com) and create a pull request (if you don't see a pop-up with suggestion to create a new branch, go to [pulls](https://github.com/cybermagnolia/cybermagnolia.com/pulls) and click on the `New pull request button`. Then select your branch as a comparison.)

![Pull request popup on GitHub](./img/pull_request.png)

5. Edit the PR - set yourself as the assignee, select reviewers, add a `blog` label. Add a brief description of the post content if you'd like and hit `Create pull request`.

![PR editing on GitHub](./img/pr_editing.png)

6. Once you create the PR, there will be some automatic checks running.

    * Make sure that the required checks pass.
    * The last check includes a deploy preview - click on the `Details` button to see the preview. Double check that everything looks good on the post, and then go to the home page and see whether the header of the post looks fine (particularly check whether the text snippet is filled out, so people want to click on the post and read more.)

![PR checks](./img/pr_checks.png)

7. If everything looks good and you'd like the post to be reviewed faster, poke your reviewers on Slack in `#organizers` channel.

8. Once the PR has been approved, go back to your pull request. Merge the PR and delete the branch - it's no longer needed and it helps us keep the repository tidy.

9. Wait a few minutes (usually 3-10) and check that the new version was successfully deployed to the [CyberMagnolia website](http://cybermagnolia.com/). If something doesn't look right - rinse and repeat. If everything looks shiny — have a coffee & cake to celebrate! Well done! :muscle: :tada: :coffee:
