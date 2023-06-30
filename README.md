# Getting Started with Create React App

## CI/CD Pipeline for React App using Github Action

https://www.youtube.com/watch?v=GqyC_R3UjjQ&t=3sts

# install react application
- npx create-react-app 
	
# use github setting > page for deploy site on github
- npm install gh-pages --save-dev

# add homepage in package.json
- "homepage": "https://JigneshpPlutus.github.io/react-cicd-demo",

# add common in package.json
"scripts": {
    "predeploy": "npm run build", 
    "deploy": "gh-pages -d build",
    "start": "react-scripts start",
    "build": "react-scripts build",
    "test": "react-scripts test",
    "eject": "react-scripts eject"
},

# deploy the project on GitHub
- npm run deploy

# Error: The deploy step encountered an error: The process '/usr/bin/git' failed with exit code 128

- Solution: https://github.com/JamesIves/github-pages-deploy-action/issues/1110
- Go to repo settings
- Select Actions -> General --> Workflow permissions, select Read and Write permissions
OR
- https://github.com/JamesIves/github-pages-deploy-action/issues/1110#issuecomment-1124787331

# unpublish the site

# For again publish you need to run action 
- https://github.com/JigneshpPlutus/react-cicd-demo/actions/workflows/pages/pages-build-deployment

