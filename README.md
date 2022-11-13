## KubeFin GitHub Workflows

These workflows are used within the KubeFin project

- [Reusable workflows](https://docs.github.com/en/actions/using-workflows/reusing-workflows) are under the `workflows` directory

  They can be used as follows:
  ```yaml
  on: [pull_request]

  jobs:
    job_name:
      steps:
      - uses: kubefin/actions/.github/workflows/xxx.yml@main  
  ```

- [Composite actions](https://docs.github.com/en/actions/creating-actions/creating-a-composite-action) have their own unique folder the root of the repo

  They can be used as follows:
  ```yaml
  on: [pull_request]

  jobs:
    job_name:
      steps:
      # ensure this is under steps
      - uses: kubefin/actions/composite/setup-ko@main
  ```