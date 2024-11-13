# ossf-tests/scorecard-action

This repo offers scheduled and on-demand e2e testing of ossf/scorecard-action.
Failures cause an issue to be created in the ossf/scorecard-action repo. (e.g. https://github.com/ossf/scorecard-action/issues/1304)
Each test is described below.

# HEAD

[scorecards-heads.yml](https://github.com/ossf-tests/scorecard-action/blob/main/.github/workflows/scorecards-head.yml)
uses that latest version of the docker image, which gets produced after each
commit merged to `main`. This allows us to test changes regularly when
developing changes, and can be run via dispatch as part of the 
ossf/scorecard-action release process. 

# Latest GitHub release

[scorecards-latest-release.yml](https://github.com/ossf-tests/scorecard-action/blob/main/.github/workflows/scorecards-latest-release.yml)
uses the last GitHub release of ossf/scorecard action. While it specifies
`ossf/scorecard-action@main`, the version is still pinned to the latest
release via the ossf/scorecard-action
[action.yaml file](https://github.com/ossf/scorecard-action/blob/873d5fdf63bc863d140f57ed481e6a297324030b/action.yaml#L54-L56).
