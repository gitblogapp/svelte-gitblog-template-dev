# GitBlog Svelte template development

This is the development source for the [user-facing Svelte template](https://github.com/gitblogapp/svelte-gitblog-template). Create blogs from that repository, not this one.

## Develop and publish

```sh
npm ci
npm run dev
npm run release:check
```

Pull requests run the complete regression suite and verify a clean exported template with a fresh `npm ci` and `npm run update:check`. After the same checks pass on `main`, GitHub Actions publishes the verified artifact to `gitblogapp/svelte-gitblog-template` automatically. PRs never receive the publishing token.

The first separated release is 2.0.0. Later main-branch publications increment the patch version automatically; increase `minimumVersion` in `distribution/config.json` for a new minor/major series. Re-running an already published source commit does nothing. Do not edit the distribution repository directly.

See [the distribution workflow](DEVELOPMENT.md) for the file boundary, credentials, stable revision contract and recovery. Blog operating instructions remain in [docs/gitblog](docs/gitblog/README.md). The exported owner's README and agent entry point live in `distribution/`.
