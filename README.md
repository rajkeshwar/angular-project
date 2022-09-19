# AngularProject

## Steps to build and deploy on gh-pages
1. Comment dist folder in .gitignore file. So that we can push the dist folder to gh-pages
2. Add the following 2 lines in package.json to set the `--base-href` and push website content to gh-pages 

Here `--base-href` is the repo-name on github
```js    
"gh-build": "ng build --output-path website --base-href /angular-project/",
"gh-pages": "npm run gh-build && git subtree push --prefix website origin gh-pages"
```

3. Commit and push push your code to git
4. Then run `npm run gh-pages`

5. You should see that gh-pages branch would be created and the content of your dist which is `website` should be present in gh-pages branch

6. Now try to access this url `https://<YOUR_GITHUB_USERNAME>.github.io/<YOUR_REPO_NAME>/`
7. For example `https://rajkeshwar.github.io/angular-project/`


