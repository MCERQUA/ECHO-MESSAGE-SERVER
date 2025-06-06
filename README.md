# ECHO-MESSAGE-SERVER

## AI Chat Message Queue & Task Management System

This repository serves as a message queue and task management system for Echo AI Systems. All client conversations and requests are stored here as markdown files for processing.

### Structure

```
├── messages/          # Individual chat messages
│   └── YYYY-MM-DD/   # Daily folders
├── tasks/            # Extracted tasks and requests
│   ├── pending/      # Tasks awaiting processing
│   ├── in-progress/  # Currently being worked on
│   └── completed/    # Finished tasks
├── conversations/    # Full conversation logs
└── system/          # System configuration and logs
```

### Message Format

Each message is stored as a markdown file with metadata:

```markdown
---
id: unique-message-id
timestamp: 2025-06-06T12:00:00Z
client: client-identifier
type: message|task|request
status: new|processing|completed
---

# Message Content

[User's message or task description]
```

### Integration

This repository is integrated with:
- **echo2.pages.dev** - AI chat interface
- **Groq API** - LLM inference
- **GitHub MCP** - Automated file management

### Usage

1. Users interact with the AI chat at echo2.pages.dev
2. Conversations and requests are automatically saved here
3. Echo AI reviews and processes tasks during sessions
4. Status updates are committed back to track progress
