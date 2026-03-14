# My GitHub Action
Automate your workflow with this simple GitHub Action.
This GitHub Action prints a friendly message whenever you push code to the repository.

## Usage

Add this to your `.github/workflows/your-workflow.yml`:

```yaml
name: Hello Workflow

on: push

jobs:
  say-hello:
    runs-on: ubuntu-latest
    steps:
      - name: Checkout repo
        uses: actions/checkout@v4

      - name: Run my Action
        uses: your-username/my-github-action@v1



> **Tip:** Replace `your-username/my-github-action@v1` with your repository path and version.

---

# 4. **Inputs** (Optional)
If your Action takes parameters, describe them clearly.

```markdown
## Inputs

| Input        | Description                     | Default |
| ------------ | ------------------------------- | ------- |
| `message`    | The message to print in console | "Hello" |


- name: Run my Action
  uses: your-username/my-github-action@v1
  with:
    message: "Hi there!"


## Outputs

| Output      | Description               |
| ----------- | ------------------------- |
| `result`    | The final printed message |


## Example

```yaml
name: Greeting Workflow

on: push

jobs:
  greet:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - name: Say Hi
        uses: your-username/my-github-action@v1
        with:
          message: "Welcome to GitHub Actions!"

```

| Event                 | Description                                 | Example Usage                                               |
| --------------------- | ------------------------------------------- | ----------------------------------------------------------- |
| `push`                | Trigger when code is pushed to repo         | `on: push`                                                  |
| `pull_request`        | Trigger when a PR is opened/updated         | `on: pull_request`                                          |
| `workflow_dispatch`   | Manual trigger from GitHub UI               | `on: workflow_dispatch`                                     |
| `schedule`            | Trigger on a cron schedule                  | `on: schedule: - cron: '0 0 * * *'` (every day at midnight) |
| `release`             | Trigger when a release is created           | `on: release`                                               |
| `issue_comment`       | Trigger when someone comments on an issue   | `on: issue_comment`                                         |
| `fork`                | Trigger when someone forks the repo         | `on: fork`                                                  |
| `create` / `delete`   | Trigger on branch/tag creation or deletion  | `on: create`                                                |
| `watch`               | Trigger when someone stars your repo        | `on: watch`                                                 |
| `pull_request_target` | Similar to PR but runs in base repo context | `on: pull_request_target`                                   |
| `deployment`          | Trigger when a deployment happens           | `on: deployment`                                            |

```

 ``` name

What it is: A human-readable label for your workflow, job, or step.
```
``` 
uses

What it is: References a prebuilt GitHub Action.

| `uses` value                  | Purpose                       |
| ----------------------------- | ----------------------------- |
| `actions/checkout@v4`         | Checks out your code          |
| `actions/setup-node@v4`       | Sets up Node.js               |
| `actions/setup-python@v5`     | Sets up Python                |
| `actions/cache@v3`            | Caches dependencies           |
| `docker/build-push-action@v5` | Builds & pushes Docker images |

```