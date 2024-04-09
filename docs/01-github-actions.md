# Introduction to Github Actions

- CI/CD platform that allows to automate your build, test and deployment pipeline
  in each pull request to your repository or deploy a merged pull request to production
- Goes beyond just DevOps and lets you run workflow other event happen in the repository.
  For example, you can run a workflow to automatically update metrics of your activity in
  Github and show them into your personal README.md section.

## Components

- _Workflow_ -> Pipeline triggered when a event occurs in your repository
- _Jobs_ -> Tasks to be performed (can run sequential or in parallel)
- _Runner_ -> Container or VM where a job is executed
- _Steps_ -> Each task performed into a runner
- _Actions_ -> Reusable extension that can simplify your workflow.


### a) Workflows

- Configurble automated process that will run one or more jobs
- Defined by a YAML file checked into `.github/workflows` directory
- A repository can have multiple workflows to perform different set of tasks

### b) Events
- Specify activity in a repository that triggers a workflow run (open a pull request,
  pushes a commit)
- Also, a workflow can be triggered by a scheduled or post to a REST API or manually.

### c) Jobs
- Set of _steps_ in a workflow that is executed __on the same runner__. Each step
  is either a shell script that will be executed, or an _action_ that willl be run.
  _Steps_ are executed in order and are dependent on each other and data can be shared
  from one step to another.
- By default, jobs have no dependencies and run in parallel with each other.
  When a job takes a dependency on another job, it will wait for the dependent job
  to complete before it can run.

### d) Actions
-   A custom application for the Github Actions platform that performs a complex
    but frequently repeated task.

### e) Runners
-   A server that runs your workflows when they are triggered. Each runner can run
    a single job at a time.
-   Github provides Ubuntu Linux, Microsoft Windows and macOS runners to run
    your workflows.



## References

<p>
    1. <a href="https://docs.github.com/en/actions/learn-github-actions/understanding-github-actions">
        Understanding Github Actions
    </a>
</p>