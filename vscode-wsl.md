✅ What You Need
- WSL installed and working
You’ve already got Ubuntu 24.04 running — great.
- VS Code installed on Windows
No need to reinstall.
- Install the “Remote - WSL” extension in VS Code
- Open VS Code
- Go to Extensions (Ctrl+Shift+X)
- Search for Remote - WSL and install it


🚀 How to Use VS Code with WSL
Once the extension is installed:
- Open VS Code
- Press Ctrl+Shift+P → type WSL → select “Remote-WSL: New Window”
- VS Code will launch a new window connected to your WSL distro
- You can now open folders like /home/jenfri/homeauto directly
Or from the terminal:
code .


This opens the current WSL folder in VS Code (if code is on your WSL path).

🧠 Bonus Tips
- You can install WSL-specific extensions (like Python, Docker) inside the WSL context
- VS Code will auto-detect your Linux environment and offer to install missing tools
- Git integration works seamlessly across WSL and Windows  





🧰 VS Code Workspace Setup for homeauto

1. 📁 Create a Workspace File

In your ~/homeauto folder (inside WSL), create:

```bash
code homeauto.code-workspace
```

Paste this:

```json
{
  "folders": [
    {
      "path": "."
    }
  ],
  "settings": {
    "files.exclude": {
      "**/.git": true,
      "**/.DS_Store": true,
      "**/node_modules": true
    },
    "editor.tabSize": 2,
    "yaml.schemas": {
      "https://json.schemastore.org/docker-compose.json": "docker-compose.yml"
    },
    "markdown.preview.scrollEditorWithPreview": true,
    "markdown.preview.openMarkdownLinks": "inEditor"
  }
}
```

This gives you:
- Clean folder view
- Docker Compose schema validation
- Markdown preview behavior tuned for docs

