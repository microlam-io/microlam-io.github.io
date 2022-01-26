# Microlam.io Website Based on Jekyll

## Getting Started

These instructions will get you a copy of the Microlam.io website up and running on your local machine for development and testing purposes.

### Installation

[Jekyll static site generator docs](https://jekyllrb.com/docs/).

1. Install a full [Ruby development environment](https://jekyllrb.com/docs/installation/). If you use `rvm`, run: `rvm use 2.7.1`.
2. Install [bundler](https://jekyllrb.com/docs/ruby-101/#bundler)  [gems](https://jekyllrb.com/docs/ruby-101/#gems)
  
        gem install bundler

3. Fork the [project repository](https://github.com/microlam-io/microlam-io.github.io), then clone your fork.
  
        git clone git@github.com:YOUR_USER_NAME/microlam-io.github.io.git

4. Change into the project directory:
  
        cd microlam-io.github.io

5. Use bundler to fetch all required gems in their respective versions

        bundle install

6. Build the site and make it available on a local server
  
        bundle exec jekyll serve

7. Now browse to http://localhost:4000

> If you encounter any unexpected errors during the above, please refer to the [troubleshooting](https://jekyllrb.com/docs/troubleshooting/#configuration-problems) page or the [requirements](https://jekyllrb.com/docs/installation/#requirements) page, as you might be missing development headers or other prerequisites.

**For more regarding the use of Jekyll, please refer to the [Jekyll Step by Step Tutorial](https://jekyllrb.com/docs/step-by-step/01-setup/).**

### Deploying to GitHub Pages

The website deployment is automatically performed by GitHub Actions (when commits are pushed to the `develop` branch).
If for some reason you need to deploy from your local machine, follow these instructions:

1. Install the [act](https://github.com/nektos/act#installation) executable to run GitHub Actions locally
2. Run `act -s GITHUB_TOKEN=<GITHUB_TOKEN>`, where *<GITHUB_TOKEN>* needs to be replaced with a token that allows you to push to the https://github.com/microlam-io/microlam-io.github.io repository.

## Writing a blog

To write a blog:

- create an author entry in [_data/authors.yaml](https://github.com/microlam-io/microlam-io.github.io/blob/develop/_data/authors.yaml)
  - `emailhash` you can get by running `echo your@email.org | md5` using an email you have registered from the [Gravatar service](https://gravatar.com),
- create an blog entry under [_posts](https://github.com/microlam-io/microlam-io.github.io/tree/develop/_posts)
  - the file name is `yyyy-mm-dd-slug.adoc`
- `tags` should be used with some care as an archive page is created for of them. Below are some basic rules to try follow:
  - `microlam-io-release` used for Microlam release blogs
  - `announcement` used for general announcement with some impact.
  - `extension` used for blogs related to a specific extension.
  - `user-story` used for stories from users/companies adopting Microlam.
  - `development-tips` used for blogs with tips to develop using Microlam or Microlam itself. 
  - add a tech specific, like `kafka`, if your post has a significant mention/relevance to that technology.
  - tags is space separated list `tags:extension grpc`
  - tags must be in lowercase
- it's in asciidoc format, there is an example as shown with [2022-01-02-microlam-0-3-2-released.adoc](https://github.com/icrolam-io/microlam-io.github.io/blob/develop/_posts/2022-01-02-microlam-0-3-2-released)
  - Be aware that the `date` attribute in the asciidoc preamble defines when the article will be published. Use a present date while writing your article to test locally, then switch to the actual target date before submitting. 
- send a pull request against the develop branch and voilà

## Contributing

Please read [CONTRIBUTING.md](https://github.com/microlam-io/microlam-io.github.io/blob/master/CONTRIBUTING.md) for details on our code of conduct, and the process for submitting pull requests to us.

## License

This website is licensed under the [Creative Commons Attribution 3.0](https://creativecommons.org/licenses/by/3.0/).
