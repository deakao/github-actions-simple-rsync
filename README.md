# github-actions-simple-rsync (self-hosted)

 .github/workflow/main.yaml
```
on: 
  push:
    branches:
      - master
jobs:
  job1:
    runs-on: self-hosted
    steps:
      - uses: actions/checkout@master
  job2:
    runs-on: self-hosted
    steps:
      - shell: bash
        run: | 
          rsync -azP --exclude '.git' ~/actions-runner/_work/repo_name/repo_name/ /var/www/
```
