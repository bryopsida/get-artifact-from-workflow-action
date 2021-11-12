# get-artifact-from-workflow-action
An action to fetch an individual artifact from a workflow at a specific revision

## How to use
Add the following step to your workflow

``` yaml
- uses: bryopsida/get-artifact-from-workflow-action@v1
  with:
    owner: '<repo owner>'
    repo: '<repo>'
    workflow: '<workflow-filename>.yml'
    token: ${{ secrets.GITHUB_TOKEN }} || '<github_pat>'
    revision: '<sha_revision>'
    artifact: '<artifact_name>'
```

The artifact will be available on the file system for your next step.