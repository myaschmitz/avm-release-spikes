# avm-release-spikes

Throwaway Phase 0 spikes for AVM release automation (azure-cloud-native/Azure-Verified-Modules#218). Nothing here is production code. Safe to delete.

Each workflow answers one question and prints `RESULT|...` lines to its log:

- `spike-d4.yml`: what `GITHUB_TOKEN` can do (state branch, tags, releases, issues, cross-repo reads, team membership).
- `spike-gate.yml`: a release gate that checks out an exact SHA, posts a check run, and reuses a passing one.
- `spike-oidc.yml`: OIDC `sub` and `job_workflow_ref` when a reusable workflow is called by branch versus by SHA.
- `spike-concurrency.yml`: how one concurrency group handles a burst of runs.
- `spike-triggers.yml`: which events fire, and whether `GITHUB_TOKEN` actions retrigger workflows.
- `spike-scheduler.yml`: real delay of a 15-minute offset cron.
Last synced by spike.
