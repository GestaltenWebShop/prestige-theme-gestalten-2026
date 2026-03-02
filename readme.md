# Git Instructions

## When Prestige releases an update

1. ### Put the new Prestige code into theme-base
   1. ```git checkout theme-base```
   2. ```shopify theme pull --theme <ID_OF_NEW_PRESTIGE_THEME>```
   3. ```git add .```
   4. ```git commit -m "Upstream: update Prestige to vX.Y.Z"```
   5. ```git push```
2. ### Merge vendor update into gestalten branch
   1. ```git checkout gestalten```
   2. ```git merge theme-base```
3. ### Resolve conflicts (usually in sections/, snippets/, assets/), then:
   1. ```git add .```
   2. ```git commit -m "Merge Prestige update from theme-base"```
   3. ```git push```
      
    