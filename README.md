# vite-demo
## Using vite in codespaces

### Configure Dev Container

- From Github repo, click on the **Code** button and then into the **Codespaces** tab. 
- Under codespaces tab click into the **3 dots** for extended functionality, and then click on **Configure dev container**

#### .devcontainer ports

Add the `portsAttributes` definition for Vite port `5173`, add a label, and force preview within the browser window. 

````json
{
  "image": "mcr.microsoft.com/devcontainers/universal:2",
  "features": {
  },
  "portsAttributes": {
    "5173": {
      "label": "Vite port",
      "onAutoForward": "openPreview"
    }
  },
  "forwardPorts": [5173]
}
````

Save your changes.

### Fire it up

- Once your .devcontainer is ready, go back to the Github repo (you'll now see the dev config) and click the **Code** button.
- Under codespaces tab click **Create codespace on main** button to launch an instance of VS code in a new tab.

### Configure Vite build

Go to the [Vite guide](https://vitejs.dev/guide/) and get the latest build commands, also RTFM.

- Run `npm create vite@latest` in your codespace terminal and then follow the prompts
- This will take a few moments, but eventually you will see the vite-project folder in your left panel
- Once your project is built, add the following flag to your package.json dev script: ` "dev": "vite --host"`
- Next, `cd` into your project and run it with with `npm run dev`

### Result

Using Vite in codespaces you can quickly and easily set up a repo with a modern and lightweight build tool and use VS Code in the browser to edit and preview.

Special thanks to [Morten Rand-Hendrickson](https://www.linkedin.com/learning/build-a-javascript-ai-app-with-react-and-the-openai-api/sidebar-build-a-react-app-using-vite-and-github-codespaces?autoSkip=true&resume=false) (for generally being awesome) and also teaching me this.
