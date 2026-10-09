# leapwork-github-action

This GitHub Action is used to run Leapwork as part of a CI/CD process.

In your GitHub repo, create a ````.github/workflows/main.yml```` file with the following content:

```yaml
name: Test Leapwork Action
on:
  push:
    branches:
      - main

permissions: write-all

jobs:
  run-action:
    name: Test with Leapwork
    runs-on: ubuntu-latest

    steps:
      - uses: actions/checkout@v3
        with:
          fetch-depth: 0

      - name: Call Leapwork GitHub Action
        uses: leapwork/Github-action@v1.0
        with:
          leapworkApiUrl: ${{ vars.LEAPWORK_API_URL }}
          leapworkApiKey: ${{ secrets.LEAPWORK_API_KEY }}
          leapworkSchedule: ${{ vars.LEAPWORK_SCHEDULE }}
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
```

Reference to Actions must include a version number. Use the newest version of the action, which is ````@v1.0```` at the time of writing.

Then add environment variables:

* ````LEAPWORK_API_URL```` - your Leapwork controller REST API url, such as ````http://<controller-ip>:<port>/api````
* ````LEAPWORK_SCHEDULE```` - the name of your Leapwork schedule

and secret:

* ````LEAPWORK_API_KEY```` - the API key to access the REST API, also referred to as the "Access Key"

Once you commit a change in your repo, the Leapwork GitHub Action will execute, running the schedule on the Controller provided. If something fails, an issue will be created in GitHub with relevant details.

- Git versioning access validated by Leapwork at 2026-09-23 06:51:33 UTC.

- Git versioning access validated by Leapwork at 2026-09-23 07:03:38 UTC.

- Git versioning access validated by Leapwork at 2026-09-23 07:53:47 UTC.

- Git versioning access validated by Leapwork at 2026-09-23 12:57:32 UTC.

- Git versioning access validated by Leapwork at 2026-09-24 12:53:41 UTC.

- Git versioning access validated by Leapwork at 2026-09-28 08:27:59 UTC.

- Git versioning access validated by Leapwork at 2026-09-28 08:44:37 UTC.

- Git versioning access validated by Leapwork at 2026-09-28 08:45:34 UTC.

- Git versioning access validated by Leapwork at 2026-09-28 08:54:05 UTC.

- Git versioning access validated by Leapwork at 2026-09-28 08:54:16 UTC.

- Git versioning access validated by Leapwork at 2026-09-28 10:29:12 UTC.

- Git versioning access validated by Leapwork at 2026-09-28 13:45:27 UTC.

- Git versioning access validated by Leapwork at 2026-09-28 14:06:56 UTC.

- Git versioning access validated by Leapwork at 2026-09-28 17:19:46 UTC.

- Git versioning access validated by Leapwork at 2026-09-28 17:45:56 UTC.

- Git versioning access validated by Leapwork at 2026-09-29 06:46:25 UTC.

- Git versioning access validated by Leapwork at 2026-09-29 12:04:15 UTC.

- Git versioning access validated by Leapwork at 2026-09-29 12:15:00 UTC.

- Git versioning access validated by Leapwork at 2026-09-29 13:22:05 UTC.

- Git versioning access validated by Leapwork at 2026-09-30 12:31:40 UTC.

- Git versioning access validated by Leapwork at 2026-09-30 12:45:25 UTC.

- Git versioning access validated by Leapwork at 2026-09-30 12:56:58 UTC.

- Git versioning access validated by Leapwork at 2026-09-30 13:22:23 UTC.

- Git versioning access validated by Leapwork at 2026-09-30 13:30:15 UTC.

- Git versioning access validated by Leapwork at 2026-10-01 11:31:28 UTC.

- Git versioning access validated by Leapwork at 2026-10-01 16:50:38 UTC.

- Git versioning access validated by Leapwork at 2026-10-01 17:01:07 UTC.

- Git versioning access validated by Leapwork at 2026-10-01 17:53:04 UTC.

- Git versioning access validated by Leapwork at 2026-10-01 18:00:47 UTC.

- Git versioning access validated by Leapwork at 2026-10-08 13:35:09 UTC.

- Git versioning access validated by Leapwork at 2026-10-08 14:01:58 UTC.

- Git versioning access validated by Leapwork at 2026-10-08 14:30:13 UTC.

- Git versioning access validated by Leapwork at 2026-10-08 14:40:37 UTC.

- Git versioning access validated by Leapwork at 2026-10-08 17:30:42 UTC.

- Git versioning access validated by Leapwork at 2026-10-09 12:57:23 UTC.
