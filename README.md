## Setup

Prereq: https://cloud.google.com/build/docs/configuring-notifications/automate#github-issues

Presume the following folder structure: 

```
.
├── cloud-build-notifiers
│   └── setup.sh
│   └── ...
└── cbn-template-1481
│   └── template.txt
│   └── config.yaml
│   └── README.md (this file)
```

Setup/resetup: 

```
cd  cloud-build-notifiers
./setup.sh githubissues ../cbn-template-1481/config.yaml  -t ../cbn-template-1481/template.txt -s github_token
```