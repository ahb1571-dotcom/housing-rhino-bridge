# Housing Rhino Bridge

Private task repository for a deliberately narrow, allowlisted bridge to one local Rhino 8 workstation.

## Security model

- The GitHub workflow never executes arbitrary commands from `current_task.json`.
- The task file may request only task types allowlisted by the **local** `run_task.ps1`.
- Scientific scripts live locally under `E:\research\housingpaper\_rhino_bridge_local`; they are not downloaded from GitHub for execution.
- The workflow has `contents: read` only.
- Results are returned as GitHub Actions artifacts.
- Do not enable pull-request triggers for this workflow.
- Keep this repository private.

## Current allowlisted tasks

- `noop`
- `health_check`
- `weather_provenance`

Use **Actions → Rhino Bridge → Run workflow** for manual execution, or update only `tasks/current_task.json` on `main` to trigger the bridge.
