# Flame of the Last Candle 🕯&#xFE0F;

Just another blog from a guy.

## Workflow
Posts are written and pushed from [Forestry.io](https://forestry.io/).

New posts are sent from Forestry to the `staging` branch. 

When time to publish one or more posts to the web, `staging` is merged to `main`. 

Finally, Netlify sees the `main` branch update, and then builds and deploys the site to [https://fotlc.netlify.app/](https://fotlc.netlify.app/).

### CL commands

```
npx eleventy
```

Or build and host locally for local development
```
npx eleventy --serve
```

Or build automatically when a template changes:
```
npx eleventy --watch
```

Or in debug mode:
```
DEBUG=* npx eleventy
