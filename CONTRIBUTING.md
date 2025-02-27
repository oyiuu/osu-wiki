Thanks for taking the time to make the osu! wiki better!

Anyone is allowed (and encouraged!) to contribute to the osu! wiki.

## Getting Started

### Markdown

The osu! wiki is formatted using Markdown (specifically [GitHub-Flavoured Markdown (GFM)](https://help.github.com/articles/getting-started-with-writing-and-formatting-on-github/)), a markup language that allows for text to have basic styling.

[adam-p's Markdown Cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet) is a fantastic tool of reference if you need to quickly learn about or refresh your memory of a Markdown feature.

### Git and GitHub

Since the osu! wiki is managed through this GitHub repository, you'll need some basic knowledge of [Git](https://git-scm.com/) in order to contribute.

Luckily, if you're not willing to get too involved with the technicalities of Git, GitHub provides some on-site tools that can help you easily make changes. The [osu! wiki contribution guide](https://github.com/ppy/osu-wiki/tree/master/wiki/osu!_wiki/Contribution_guide) explains step-by-step how to utilise them in order to make changes to the osu! wiki, assuming that you have no prior knowledge of Git or GitHub.

## Standards and Requirements

The [Article Styling Criteria (ASC)](https://github.com/ppy/osu-wiki/tree/master/wiki/Article_styling_criteria) is a set of standards that must be adhered to for all new and edited articles going forward. Among these are rules regarding project structure, usage of Markdown, formatting, diction and grammar. Please refer to it if you have any specific questions or concerns.

The ASC is fairly verbose and encompasses many minute details, that are not necessary to memorise in order to take the first step of contributing to the osu! wiki. Have a look at the [contribution guide](https://github.com/ppy/osu-wiki/tree/master/wiki/osu!_wiki/Contribution_guide), and other contributors will also be happy to answer your questions in the `#osu-wiki` channel of the [osu!dev Discord server](https://discord.gg/ppy).

## Testing

All pull requests are automatically run through a series of continuous integration checks (CI) in order to catch various common errors.

For people familiar with the command line, these CI checks can also be run locally.

### Requirements

- [Python](https://www.python.org/) 3.x
- [Node.js](https://nodejs.org/) 16+ (installing via [nvm](https://github.com/nvm-sh/nvm) is recommended)

### Setup

```sh
python3 -m venv ./.venv
.venv/bin/pip3 install -r scripts/requirements.txt
npm install
```

### Running

Using `git add`, stage or commit files you want to have checked, then run from the repository root on your feature branch:

```sh
bash run-ci.sh
```
