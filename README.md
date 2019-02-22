# All Xamarin University course exercises

This repository is a helper for working with all the Xamarin University course exercise repositories. It is intended for the [Xamarin University curriculum team](https://university.xamarin.com/team) but is available for anyone to use.

## How do I use this repo?

All of the other course repositories are [Git submodules](https://git-scm.com/book/en/v2/Git-Tools-Submodules) of this repository. In order to retrieve all course repositories with it, you need to both clone this repo and retrieve all submodule content. This can be done in many Git GUI applications with a few clicks, but can also be accomplished with the following Git commands.

```bash
git clone {this-repository-URL}
cd {new-cloned-repo-path}
git submodule init
git submodule update
```

## How do I add a new course?

1. Create a [new repo](https://github.com/organizations/XamarinUniversity/repositories/new) with a name to match the course ID (e.g., XAM123 or IOS234)
2. Create a new git repo locally: `git init` in your desired course ID folder
3. Copy over a **LICENSE** and **.gitignore** from another course
4. Copy over a **README.md** file and **.github** directory from another course, editing the course information (ID, title, GitHub organization, and proposed GitHub repo URL)
5. Commit your new files to the repo and push your commits to the new repo created above
6. Add a submodule in this repo to the new course repo's master branch: `git submodule add -b master {course-repo-clone-url.git}`
7. Commit and push the submodule changes to this repo (or submit a pull request)
