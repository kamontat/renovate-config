# renovate-config
Custom Renovate Configuration

## What?

```json
{
  "extends": [
    "config:base",
    ":rebaseStalePrs",
    ":assignAndReview(kamontat)",
    ":automergeMinor",
    ":automergeDigest",
    ":automergeBranchPush",
    ":pinSkipCi",
    ":prConcurrentLimit10",
    "schedule:nonOfficeHours",
    "group:allNonMajor"
  ],
  "labels": ["bot", "dependencies"]
}
```

1. `config:base` - base configuration provide by renovate. [presets-config](https://renovatebot.com/docs/presets-config)
2. `:rebaseStalePrs` - Rebase existing PRs any time the base branch has been updated. [rebasestaleprs](https://renovatebot.com/docs/presets-default/#rebasestaleprs)
3. `:assignAndReview` - Set arg0 as assignee and reviewer of PRs. [assignandreview](https://renovatebot.com/docs/presets-default/#assignandreviewltarg0gt)
4. `:automergeMinor` - Automerge patch and minor upgrades if they pass tests. [automergeminor](https://renovatebot.com/docs/presets-default/#automergeminor)
5. `:automergeDigest` - Automerge digest upgrades if they pass tests. [automergedigest](https://renovatebot.com/docs/presets-default/#automergedigest)
6. `:automergeBranchPush` - If automerging, push the new commit directly to base branch (no PR). [automergebranchpush](https://renovatebot.com/docs/presets-default/#automergebranchpush)
7. `:pinSkipCi` - Add [skip ci] to commit message body whenever pinning. [pinskipci](https://renovatebot.com/docs/presets-default/#pinskipci)
8. `:prConcurrentLimit10` - Limit to maximum 10 concurrent Renovate PRs at any time. [prconcurrentlimit10](https://renovatebot.com/docs/presets-default/#prconcurrentlimit10)
9. `schedule:nonOfficeHours` - Schedule for typical non-office hours (night time and weekends). [schedulenonofficehours](https://renovatebot.com/docs/presets-schedule/#schedulenonofficehours)
10. `group:allNonMajor` - Group all minor and patch updates together. [groupallnonmajor](https://renovatebot.com/docs/presets-group/#groupallnonmajor)
11. `labels` - Labels to add to Pull Request. [labels](https://renovatebot.com/docs/configuration-options/#labels)

## Usage

```json
{
  "extends": "github>kamontat/renovate-config"
}
```
