# AngularProject

## Steps to build and deploy on gh-pages
Add following line in package.json

Here `--base-href` is the repo-name on github
```js    
"gh-build": "ng build --output-path website --base-href /angular-project/",
"gh-pages": "npm run gh-build && git subtree push --prefix website origin gh-pages"
```

Commit and push push your code to git
Then run `npm run gh-pages`

You should see that gh-pages branch would be created and the content of your dist which is `website` should be present in gh-pages branch

Now try to access this url `https://<YOUR_GITHUB_USERNAME>.github.io/<YOUR_REPO_NAME>/`
For example `https://rajkeshwar.github.io/angular-project/`


