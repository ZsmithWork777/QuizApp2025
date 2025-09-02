## Run
npm i
npm run dev    # http://localhost:5173

## Build
npm run build  # outputs to dist/

## Deploy to GitHub Pages
# one-time in Settings → Pages: branch=gh-pages, folder=/ (root)
npm run build
git checkout gh-pages || git checkout --orphan gh-pages
git reset --hard
git --work-tree dist add --all
git --work-tree dist commit -m "deploy"
git push -f origin HEAD:gh-pages
git checkout -f main