# 📄 File Summarizer MCP Server

A custom MCP (Model Context Protocol) server that reads and summarizes the contents of any file type (PDF, DOCX, TXT, HTML, JSON, etc.) using Apache Tika, with optional multilingual support.

> 🧠 Easily plug this into Claude Desktop or other LLM tools to enable file-based context and summarization.

---

## 🚀 Features

- 🔍 Reads content from any file type supported by **Apache Tika**
- ✨ Summarizes file content or raw input text
- 🌍 Auto-detects file language and translates non-English text before summarizing
- 🌐 Optional MCP tools to detect language and translate text
- 🧩 Async MCP tools for smooth integration
- 🛠️ Built with **Python 3.12** and the [FastMCP](https://github.com/modelcontext/fastmcp) framework
- ✅ Ready for use with Claude Desktop or any other MCP client
- 📦 Published to PyPI for easy installation

---

## 📦 Installation

### From PyPI

```bash
pip install file-summarizer-mcp-server
````

### From GitHub

```bash
git clone https://github.com/Muskan244/File_Summarizer_MCP_Server.git
cd File_Summarizer_MCP_Server
uv venv
source .venv/bin/activate  # or .venv\Scripts\activate on Windows
uv pip install -r requirements.txt
```

---

## 🛠 Claude Desktop Integration

To use this server inside Claude Desktop:

1. Open (or create) your Claude config:

#### macOS

```bash
code ~/Library/Application\ Support/Claude/claude_desktop_config.json
```

#### Windows

```bash
code $env:AppData\Claude\claude_desktop_config.json
```

2. Add your server entry:

```json
{
  "mcpServers": {
    "file-summarizer": {
      "command": "uv",
      "args": [
        "--directory",
        "/ABSOLUTE/PATH/TO/File_Summarizer_MCP_Server/file_summarizer",
        "run",
        "file_summarizer.py"
      ]
    }
  }
}
```

3. Restart Claude Desktop, and your tools should appear!

---

## 🧪 MCP Tools Provided

| Tool Name                   | Description                        |
| --------------------------- | ---------------------------------- |
| `read_file`                 | Reads raw content from a file      |
| `summarize_file`            | Summarizes content of any file     |
| `summarize_text`            | Summarizes raw text string         |
| `detect_language`           | Detects the language of input text |
| `translate_text`            | Translates any text to English     |
| `transcribe_file`           | Transcribe audio or video file content    |

---

## 📝 Requirements

* Python 3.12
* Apache Tika
* langdetect
* deep-translator
* fastmcp

Install all with:

```bash
pip install -r requirements.txt
```

---

## 📜 License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

## 👤 Author

[Muskan Raghav](https://github.com/Muskan244)
