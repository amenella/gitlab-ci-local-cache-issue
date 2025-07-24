# gitlab-ci-local-cache-issue

Temporary repository to report an issue on https://github.com/firecow/gitlab-ci-local/issues.

The issue concerns cache handling, and seems to have been introduced since gitlab-ci-local@v4.54.0

**Current branch (`master`)** is using latest version (gitlab-ci-local@v4.61.0) and **is failing**.

Other branch (`valid-ci`) is using an old version (gitlab-ci-local@v4.54.0) and has the expected behaviour.

## Usage

To reproduce issue :

```bash
git switch master
npm ci
npx gitlab-ci-local
# (branch master) pipeline is failing

git switch valid-ci
npm ci
npx gitlab-ci-local
# (branch valid-ci) pipeline is successful
```
