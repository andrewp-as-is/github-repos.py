<!--
https://readme42.com
-->


[![](https://img.shields.io/pypi/v/github-repos.svg?maxAge=3600)](https://pypi.org/project/github-repos/)
[![](https://img.shields.io/badge/License-Unlicense-blue.svg?longCache=True)](https://unlicense.org/)
[![](https://github.com/andrewp-as-is/github-repos.py/workflows/tests42/badge.svg)](https://github.com/andrewp-as-is/github-repos.py/actions)

### Installation
```bash
$ [sudo] pip install github-repos
```

#### Config
bash|python
-|-
`export GITHUB_TOKEN="your_github_token"`|`os.environ["GITHUB_TOKEN"]="your_github_token"`

#### Examples
delete orphaned repos (if basename = repo name)

```bash
$ cd ~/git/owner
$ python -m github_repos | awk -F '/' '{print $2}' | grep -v -iF "$(ls -1)" | xargs python -m github_delete
```

<p align="center">
    <a href="https://readme42.com/">readme42.com</a>
</p>