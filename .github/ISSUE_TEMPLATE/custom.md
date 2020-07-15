---
name: Custom issue template
about: Describe this issue template's purpose here.
title: ''
labels: ''
assignees: ''

---

This repository's issues are reserved for feature requests, and bug reports, and questions.

## I'm submitting a ...
  - [x] bug report
  - [ ] feature request
  - [ ] question


## Expected Behavior
When I build and push the website, I begin in the source branch and use a Rakefile to automate the building and pushing, like so:

```
cd arfc.github.io
git checkout source
git push origin source
rake publish
```

 I expect that there will be neither errors nor warnings when I do this.

## Actual Behavior
I get this warning:
 
```
/Users/huff/.gem/gems/jekyll-4.0.0/lib/jekyll/convertible.rb:41: warning: Using the last argument as keyword parameters is deprecated
```

## Steps to Reproduce the Problem

```
cd arfc.github.io
git checkout source
git push origin source
rake publish
```

## Specifications

  - Version:
     - ruby 2.7.1p83 (2020-03-31 revision a0c7c23c9c) [x86_64-darwin19]
     - jekyll 4.0.0
     - rake, version 13.0.1

  - Platform:
    - Mac (High Sierra?)



## How can this issue be closed?
This issue can be closed with a PR to the source branch that fixes the _config.yml configuration file (if it is at fault, which I suspect it is) so that this warning no longer occurs. OR, an investigation that identifies the root of the warning as system-related (is this caused by me not running the most recent version or compatible versions of ruby or Jekyll?).
