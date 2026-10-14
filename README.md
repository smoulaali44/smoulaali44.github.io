# Moula Ali S | QA Automation Portfolio

Static site, no build step. Files: `index.html`, `photo.jpg`, `Moula_Ali_Resume.docx`.

## GitHub Pages (free)
1. Create a public repo named `YOUR-USERNAME.github.io`
2. Upload all files in this folder
3. Settings > Pages > Deploy from a branch > `main` / (root)
4. Live at `https://YOUR-USERNAME.github.io` in about a minute

## GitLab Pages (free)
Add `.gitlab-ci.yml`:
```yaml
pages:
  stage: deploy
  script:
    - mkdir public
    - cp index.html photo.jpg Moula_Ali_Resume.docx public/
  artifacts:
    paths: [public]
  rules:
    - if: $CI_COMMIT_BRANCH == "main"
```
