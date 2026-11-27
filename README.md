# Prompt Manager

Prompt Manager is a lightweight Python library for managing versioned prompts, designed to streamline and automate prompt management for developers working with language models.

## Features

- **Simplified Prompt Management:** Define, update, and retrieve prompts with ease.
- **Built-In Version Control:** Automatically track prompt iterations to ensure consistency.
- **Scalable Architecture:** Manage prompts across multiple projects effortlessly.

## Installation

Install via pip:

```bash
pip install prompt-manager
Usage
```


Here's a quick example:

```python
import prompt_manager

# Initialize the prompt manager with your prompts directory
manager = prompt_manager.PromptManager("prompts")

# Add version 1.0.0 of a prompt
manager.add_prompt_version(
    "welcome_message",
    "1.0.0",
    "Hello, {name}! Welcome to our platform.",
    ["name"],
    "Basic welcome message"
)

# Update with version 1.1.0
manager.add_prompt_version(
    "welcome_message",
    "1.1.0",
    "Hi, {name}! We're glad you're here. Start exploring {platform}!",
    ["name", "platform"],
    "Enhanced welcome message"
)

# Retrieve the latest version with variables injected
print(manager.get_prompt("welcome_message", {"name": "Alice", "platform": "PromptManager"}))
```
Real-World Impact
By automating prompt management, Prompt Manager reduces manual overhead, ensures prompt consistency, and enables developers to focus on improving language model applications rather than managing configuration details.

Contributing
Contributions are welcome! Please check the GitHub repository for contribution guidelines.

License
This project is licensed under the MIT License.
