# Projects

A website that showcases projects! **If you want to use it and it's not exactly
fitting your purpose, please do make upstream changes. We expect this project
to be of use to others and we're happy to make it more generic so it's easier
to adapt to other organizations.** 


## Purpose

This page was designed for &lambda; SoC. It is based off of a Coala's GSoC portal.

Why?

- It's way more appealing to students.
- You can search and filter projects.
- Project ideas as structured data are more concise and you're sure to have all
  points covered - at the same time we can show students an overview and showing
  the full information only when needed.
- A proper review process can be used for triaging and iterating on project
  ideas.
- Stop wasting time maintaining a mentors list. This can be generated from the
  projects.

## Usage

To clone the repository and run this website on your local machine, type the following commands:

    $ git clone https://github.com/LambdaIITH/iithsoc-ideas.git
    $ cd iithsoc-ideas
    $ python -m SimpleHTTPServer 8080


Then you can simply go to either of the following addresses in your browser to access the site:

    0.0.0.0:8080
    127.0.0.1:8080

## Defining Projects

Mentors and admins can define projects as JSON using the following structure:

```json
{
  "name" : "Write Project Name Here",
  "desc" : "Write a one line Description of Project here.",
  "requirements" : [
    "The applicant has to fulfill this to get started."
  ],
  "difficulty" : "low|medium|high",
  "issues" : [
    "https://github.com/LambdaIITH/iithsoc-ideas/issues/####"
  ],
  "mentors" : [
    "blabla",
    "blublu12356"
  ],
  "initiatives" : ["LambdaSoC"],
  "tags" : ["Plugins", "CI"],
  "markdown" : "Add the markdown file in data/projects/ directory. The name of that .md file should come here.",
  "collaborating_projects" : ["Add umbrella and sub-orgs here"]

}
```

Sample Markdown File

This file should contain Project Description and Milestones in following format.
_You should have atleast these three milestones for &lambda; SoC projects._

```

#### Milestones

##### COMMUNITY BONDING

* Conceptual work should be finished.
* The student have a repository, know how to work with the community.
* The applicant should know the community.

##### MIDTERM

* Everything listed here has to be reviewed and merged by midterm.
* No exceptions to that. Changing the goals is possible together with mentors.
* Yes, that includes tests and documentation.

##### FINAL

* Everything has to be reviewed and merged.
* Including tests and docs, again.

```
