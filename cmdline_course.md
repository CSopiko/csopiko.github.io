---
layout: default
---

# Command Line Tools for Linguists

This course introduced the essential tools and workflows that linguists can use to process and analyze text data efficiently in UNIX-like command line environments. Over several modules I learned not only how to use specific tools but also how to think about automation and version control.

## Module 1: Introduction to Command Line Environments

In the first week, I set up my UNIX environment by downloading Ubuntu on Windows and learned the basic commands that interact with the file system. Specifically, creating, moving, and deleting files, and understanding directory structures. I also got familiar with file permissions and the idea of users and groups in UNIX systems.

Reflecting on this week, I learned that understanding the command line is about awareness, meaning to know exactly what each command does before running it.

Example command:

```bash
echo "Hello, World" > hello.txt
```

This is a simple, yet useful command that uses the `echo` command to write the text `Hello, World` to a file called `hello.txt` using output redirection (`>`).

## Module 2: Text Processing in UNIX

This week focused on using UNIX commands like `grep`, `sed`, `cut`, and `sort` for linguistic text analysis. I learned about character encodings (`ASCII`, `UTF-8`) and how to transform and clean raw text efficiently using pipes and redirections. These tools turned large text files into structured linguistic data. I've also learned that sometimes regex could be hard.


<img src="assets/images/regular_expressions.png" alt="Photo" hspace="10" width="70%" align="mid"/>

I realized how powerful simple tools can be when combined, and that most text-processing problems can be solved without high-level programming.

Example command:

```bash
grep '^[A-Z]' text.txt | sort | uniq -c > uppercase_freqs.txt
```

This pipeline finds all lines starting with uppercase letters, sorts them, removes duplicates, and counts their frequencies, which is typical in corpus preparation.

## Module 3: Scripting, Configuration Files, and Installing Programs

Here I learned to automate workflows by writing shell scripts and managing environment variables in configuration files like `.bashrc`. Understanding `if` statements, loops, and command substitution made it possible to create reusable tools. I also practiced installing software using `apt-get`, `brew`, and `pip`.
This week taught me that scripting is about reducing repetition and making my work reproducible across systems.

Example command:

```bash
#!/bin/bash
if [ -z "$1" ]; then
    echo "Usage: $0 filename"
else
    wc -l "$1"
fi
```

This script checks if a filename is provided and counts its lines. It shows conditional logic and parameter handling.

## Module 4: Using SSH, SCP, and Version Control

This module introduced remote work and collaboration tools like `ssh`, `scp`, and Git, GitHub. I learned to connect to the servers, transfer files securely and manage projects using version control. Concepts like commits, branches, merges, and reverts became part of my workflow.

Reflecting on this week, I understood that Git is a way to track and communicate the evolution of work.

Example commands:

| Command                      | Description                  |
| ---------------------------- | ---------------------------- |
| `ssh user@server`            | Connects to a remote server  |
| `scp file user@server:/path` | Copies files securely        |
| `git commit -m "message"`    | Records a version checkpoint |

## Final Project: Building Webpages with Jekyll and GitHub Pages

In the final week, I combined all my skills to build a personal website using [Jekyll](https://jekyllrb.com/) and [GitHub Pages](https://docs.github.com/en/pages/getting-started-with-github-pages/what-is-github-pages). I learned how markdown is converted into HTML through templates and layouts (`_layout/default.html`) and how repositories host and publish static websites.

This project showed how command-line skills, version control, and automation intersect to hosting static web-pages.

## Main Takeaways

* Learned to automate linguistic data processing using UNIX tools.
* Understood how scripts, Git, and Jekyll combine into a full research workflow.
* Became comfortable working entirely in the command line.