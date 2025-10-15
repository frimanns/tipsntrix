🧰 VS Code Workspace Setup for homeauto
1. 📁 Create a Workspace File
In your ~/homeauto folder (inside WSL), create:
code homeauto.code-workspace


Paste this:

```bash
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
