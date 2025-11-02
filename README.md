# Claude Gitignore Skill

A Claude **Agent Skill** that automatically generates a `.gitignore` file for any project using the official [gitignore.io](https://docs.gitignore.io/install/command-line) service.

---

## 🚀 Overview

This skill enables Claude (or Claude Code) to detect your project stack (Java, Gradle, Node, Python, etc.) and create a tailored `.gitignore` file automatically.

It uses the [`gi`](https://docs.gitignore.io/install/command-line) command-line utility when available, or falls back to `curl` if not installed.

---

## 📂 Repository Structure



claude-gitignore-skill/
├── SKILL.md                   # Defines skill metadata and logic
├── README.md                  # You're reading this file
├── LICENSE                    # MIT License (default)
├── scripts/
│   └── generate_gitignore.sh  # Bash script used by the skill
└── examples/
└── sample-output.gitignore

## ⚙️ Installation

### 1. Install `gi` command-line tool (optional but recommended)

```bash
curl -L https://www.toptal.com/developers/gitignore/install.sh | sh
```

### 2. Clone this Skill

```bash
git clone https://github.com/didoux/claude-gitignore-skill.git
```

### 3. Move it into your Claude Skills directory

**For personal use:**

```bash
mkdir -p ~/.claude/skills/
mv claude-gitignore-skill ~/.claude/skills/
```

**For project/team use:**

```bash
mv claude-gitignore-skill .claude/skills/
```

Claude (or Claude Code) will automatically detect it and activate the Skill when your prompts match its description.

---

## 🧠 Usage Examples

Ask Claude:

> “Use the `gitignore-generator` skill to create a `.gitignore` for a Java + Maven + Docker project.”

or

> “Generate a `.gitignore` for my Python + Flask + VSCode setup.”

Claude will:

1. Detect your stack.
2. Call `gi` or `curl` to create `.gitignore`.
3. Confirm completion.

---

## 🛠️ Manual CLI Usage

You can also use the script directly:

```bash
cd claude-gitignore-skill/scripts
./generate_gitignore.sh "java,maven,docker,intellij"
```

**Example output:**

```bash
✅ .gitignore generated successfully for: java,maven,docker,intellij
```

---

## 📜 License

MIT License © 2025 [didoux](https://github.com/didoux)

---

## 🌟 Future Enhancements

* 🔍 Auto-detect languages (scan for `pom.xml`, `build.gradle.kts`, etc.)
* 🧩 Add support for `.editorconfig` and `.gitattributes`
* 🤖 Integration with a future `repo-initializer-skill` (planned)

```
