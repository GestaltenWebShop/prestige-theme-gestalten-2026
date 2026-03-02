# GIT WORKFLOW

## When Prestige releases an update

1. ### Put the new Prestige code into theme-base
   1. ```git checkout theme-base```
   2. ```shopify theme pull --theme <ID_OF_NEW_PRESTIGE_THEME>```
   3. ```git add .```
   4. ```git commit -m "Upstream: update Prestige to vX.Y.Z"```
   5. ```git push```

2. ### Put the new Prestige code into theme-base (prestige-10.11.1)
   1.```git tag prestige-X.Y.Z```
   2.```git push origin prestige-X.Y.Z```

3. ### Merge vendor update into gestalten branch
   1. ```git checkout gestalten```
   2. ```git merge theme-base```
   
4. ### Resolve conflicts (usually in sections/, snippets/, assets/), then:
   1. ```git add .```
   2. ```git commit -m "Merge Prestige update from theme-base"```
   3. ```git push```

# Shopify CLI

## How to View Your Website

1. ## Go into your theme folder and ensure in correct branch
   1. ```cd /Users/mattdavis/Sites/prestige-theme-gestalten-2026-2```
   2. ```git checkout gestalten```
2. ## Login to the store (only needed occasionally)
   1. ```shopify auth login```
3. ## Start the local development server
   1. ```shopify theme dev```

## If You Ever See Login Errors
1. ```shopify logout```
2. ```shopify login --store your-store.myshopify.com```
