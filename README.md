# Claude Gitignore Skill

A Claude **Agent Skill** that automatically generates a `.gitignore` file for any project using the official [gitignore.io](https://docs.gitignore.io/install/command-line) service.

---

## 🚀 Overview

This skill enables Claude (or Claude Code) to detect your project stack (Java, Gradle, Node, Python, etc.) and create a tailored `.gitignore` file automatically.

It uses the [`gi`](https://docs.gitignore.io/install/command-line) command-line utility when available, or falls back to `curl` if not installed.

---

## 📂 Repository Structure

