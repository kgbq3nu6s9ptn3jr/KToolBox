<p style="text-decoration:none">
  <img src="https://cdn.jsdelivr.net/gh/Ljzd-PRO/KToolBox@latest/static/repository-open-graph-2.svg" alt="logo">
</p>

<h1 style="text-align: center">
  KToolBox
</h1>

<p style="text-align: center">
  KToolBox is a useful CLI tool for downloading posts content in
  <a href="https://kemono.su/">Kemono.party / Kemono.su</a>
</p>

<p style="text-align: center">
  <a href="https://pypi.org/project/ktoolbox" target="_blank">
    <img src="https://img.shields.io/github/v/release/Ljzd-PRO/KToolBox?logo=python" alt="Version">
  </a>

  <a href="https://github.com/Ljzd-PRO/KToolBox/blob/master/LICENSE">
    <img src="https://img.shields.io/github/license/Ljzd-PRO/KToolBox" alt="BSD 3-Clause"/>
  </a>

  <a href="https://github.com/Ljzd-PRO/KToolBox/activity">
    <img src="https://img.shields.io/github/last-commit/Ljzd-PRO/KToolBox/devel" alt="Last Commit"/>
  </a>

  <a href="https://codecov.io/gh/Ljzd-PRO/KToolBox" target="_blank">
      <img src="https://codecov.io/gh/Ljzd-PRO/KToolBox/branch/master/graph/badge.svg?token=5XK9CYQHQN" alt="codecov"/>
  </a>

  <a href='https://ktoolbox.readthedocs.io/'>
    <img src='https://readthedocs.org/projects/ktoolbox/badge/?version=latest' alt='Documentation Status' />
  </a>

  <a style="text-decoration:none">
    <img src="https://img.shields.io/badge/Platform-Windows%20|%20Linux%20|%20macOS-blue" alt="Platform Win | Linux | macOS"/>
  </a>
</p>

## Features

- Supports concurrent downloads  
- Automatically retries API calls and downloads after failures  
- Allows downloading individual posts or **all posts** of a specified artist  
- Can **update downloaded** artist directories to the latest state  
- Supports customizable **file and directory naming formats** and **directory structures** for downloaded posts/artists  
- Enables excluding **specified file formats** or downloading only specified formats  
- Allows searching for artists and posts, with options to export results  
- Compatible with all platforms, with iOS shortcuts provided  
- For support related to _Coomer.su / Coomer.party_, please refer to the documentation: [Coomer](https://ktoolbox.readthedocs.io/latest/coomer/)

## Tutorial

### Installation

You can use executables from [releases](https://github.com/Ljzd-PRO/KToolBox/releases) page

=== "Manually Install - Normal"
    Recommend to use pipx
    ```bash
    pip3 install pipx
    pipx install ktoolbox
    ```

=== "Manually Install - For iOS a-Shell"
    ```bash
    pip3 install ktoolbox-pure-py
    ```
    !!! info "About a-Shell"
        [a-Shell](https://github.com/holzschu/a-shell) is an iOS terminal App, 
        it can only run pure python scripts.

### Command

For more information, use the help command or goto [Commands](commands/guide.md) page.
  
#### ❓ Get general help
```bash
ktoolbox -h
```
  
#### ❓ Get help of a command
```bash
ktoolbox download-post -h
```

#### ⬇️🖼️ Download a specific post
```bash
ktoolbox download-post https://kemono.su/fanbox/user/49494721/post/6608808
```
??? info "If some files failed to download"
    If some files failed to download, you can try to execute the command line again, 
    the downloaded files will be **skipped**.
  
#### ⬇️🖌️ Download posts from a creator
```bash
# Download all posts of the creator/artist
ktoolbox sync-creator https://kemono.su/fanbox/user/9016

# Download latest 10 posts of the creator/artist
ktoolbox sync-creator https://kemono.su/fanbox/user/9016 --length=10

# Download latest No.11-No.15 posts of the creator/artist
ktoolbox sync-creator https://kemono.su/fanbox/user/9016 --offset=10 --length=5

# Download posts from the creator/artist from 2024-1-1 to 2024-3-1
ktoolbox sync-creator https://kemono.su/fanbox/user/9016 --start-time=2024-1-1 --end-time=2024-3-1
```

### Configuration

- Download 10 files at the same time
- Rename attachments in numerical order
- Prefix the post directory name with its release/publish date
- ...

Goto [Configuration-Guide](https://ktoolbox.readthedocs.io/latest/configuration/guide/) page for more details.
