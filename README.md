## Setup

Prereq: 
  * https://cloud.google.com/build/docs/configuring-notifications/automate#github-issues
  * Cloud Build trigger to run `failure.yaml` on push to latest. 

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

Note: some elements will fail on re-apply  (e.g. re-creating service account, pubsub topic), but these are fine. 

Then, commit changes to latest branch. If setup correctly, new issue will be created. 