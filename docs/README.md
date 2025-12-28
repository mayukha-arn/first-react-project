# Setting Up React App to be Deployed in GitHub Pages

__PreReq: Check Version History (Optional)__
1. Node
   - node --version
2. npm
   - npm --version
3. Git
   - git --version

__Procedure:__
1. Create React app: this creates a new folder with the app name containing the app source code
   - *JavaScript:* npx create-react-app app-name
   - *TypeScript:* npx create-react-app app-name --template typescript
2. Enter the folder
  - cd app-name
3. Install gh-pages package: this installs the npm package & app's dependence on it is documented in package.json file
  - npm install gh-pages --save-dev
4. Add homepage:
  - enter "package.json" in CMD (opens the package)
  - add homepage property between version & private (format: https://{username}.github.io/{repo-name})
5. Add deployment scripts:
  - still within package.json
  - add predeploy & deploy property to script object
      - "predeploy": "npm run build", "deploy": "gh-pages -d build",
  - save file
6. Add "remote" that points to GitHub repository
  - git remote add origin https://github.com/{username}/{repo-name}.git
7. Push React app to GitHub repo
  - npm run deploy
  - npm run deploy -- -m "Deploy React app to GitHub Pages"
8. Configure GitHub Pages
  - in GitHub Web Browser, navigate to repo
  - above code browser, go to "Settings" tab
  - sidebar --> "Code and Automation" --> "Pages"
  - configure "Build and deployment" settings
      - Source: deploy from branch
      - Branch:
          - branch: gh-pages
          - folder: /root
          - save
9. (Optional) Store React Source Code on GitHub
  - git add .
  - git commit -m "Configure React app for deployment to GitHub Pages"
  - git push origin master
 
*Remember:* 
-  the branch "gh-pages" is to internally run the app on GitHub pages
-  for more detailed instructions, refer to: https://github.com/gitname/react-gh-pages/blob/master/README.md

# Essential JavaScript
