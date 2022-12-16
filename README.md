# VisWiz.io Build Github Action

A [Github Action](https://github.com/actions) for creating a new [VisWiz.io](https://www.viswiz.io/) build.

<img src="https://www.viswiz.io/assets/logos/viswiz-500x500-dark.png" width="200" />

## Usage

1. Create a [VisWiz.io](https://www.viswiz.io/) account.
2. Grab your VisWiz.io [API key](https://app.viswiz.io/account) and save it to your GitHub repository’s **Settings → Secrets**.
2. Create a VisWiz.io project and grab the project's ID, and optionally save it to your GitHub repository’s **Settings → Secrets**.

For example, the following workflow creates a new Buildkite build on every commit:

```yaml
- uses: viswiz-io/github-action@v1
  with:
    api-key: ${{ secrets.VISWIZ_API_KEY }}
    images-directory: ./output/
    project-id: ${{ secrets.VISWIZ_PROJECT_ID }}
```

## Inputs

| Input | Description |
| - | - |
| api-key | The API key to use when creating a new build |
| images-directory | The folder containing the images for the new build |
| project-id | The project ID containing the new build |

## Contributing

* Fork this repository.
* Create a new branch for your work.
* Push up any changes to your branch, and open a pull request.

## Releasing

* Create a new GitHub release.
