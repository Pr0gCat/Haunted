# 👻 Haunted CLI - Spectral Software Solutions

**Your codebase just got possessed by supernatural development powers.**

Transform your development workflow with an autonomous AI spirit that thinks, codes, and ships features while you focus on the bigger picture. Haunted doesn't just assist - it possesses your repository and handles complete development cycles from planning to deployment.

**🌙 No API Séance Required** - Seamlessly channels your Claude Code authentication for effortless spectral integration.

[![npm version](https://badge.fury.io/js/haunted-cli.svg)](https://badge.fury.io/js/haunted-cli)
[![TypeScript](https://img.shields.io/badge/TypeScript-007ACC?logo=typescript&logoColor=white)](https://www.typescriptlang.org/)
[![Node.js](https://img.shields.io/badge/Node.js-43853D?logo=node.js&logoColor=white)](https://nodejs.org/)

## 🔮 Supernatural Features

- **👻 Spectral Authentication**: No API keys needed - channels your Claude Code powers directly
- **🎭 Autonomous Possession**: AI takes complete ownership of features from concept to deployment
- **🌙 Concurrent Hauntings**: Multiple issues developed simultaneously across your codebase
- **🕯️ Self-Exorcising**: When bugs appear, the spirit debugs and fixes itself automatically
- **🦇 Git Manifestation**: Automatic branch creation, testing, and merging with ghostly precision
- **👺 Issue-Driven Séances**: All development starts from clear issue descriptions and priorities
- **🎃 Spectral Workflow**: Complete development lifecycle - Plan → Code → Test → Debug → Ship
- **📡 MCP Integration**: Model Context Protocol server for direct Claude communication

## 🕯️ Summoning Requirements

- **Node.js 20+** - The vessel for spectral powers (TypeScript edition)
- **Claude Code CLI** - Your gateway to the supernatural realm

## 🎭 Possession Ritual

```bash
# Global spectral possession
npm install -g haunted-cli

# Or channel directly with npx
npx haunted-cli

# For development possession
git clone <repository-url>
cd haunted
npm install
npm run build
```

**🌙 The possession is complete!** No API keys needed - Haunted channels your Claude Code authentication automatically.

### 🔮 Confirm the Haunting

```bash
# Test the spectral connection
haunted --help

# Or with npx
npx haunted-cli --help
```

## 🌙 Summoning Your Spectral Developer

### 1. Begin the Possession

```bash
# Invite the spirit into your project
haunted init
```

This spectral ritual will:
- Manifest `.haunted/` sanctuary with database and config
- Verify your Git repository is ready for haunting
- Establish supernatural configuration

### 2. Whisper Your Desires

```bash
# Communicate your high-priority wish to the spirit
haunted issue create "Implement user authentication" --priority high --description "Add login/logout functionality with JWT tokens"

# Organize supernatural work into phases
haunted phase create "Phase 1 - Core Features" --description "Essential features for MVP"

# Channel additional requests into specific phases
haunted issue create "Add password reset" --phase <phase-id> --priority medium
```

### 3. Release the Autonomous Spirit

```bash
# Unleash your spectral developer
haunted start
```

Your ghostly assistant will:
- Scan for open Issues by supernatural priority
- Manifest Git branches for each spectral task
- Possess your codebase through the complete development cycle
- Automatically merge completed hauntings

### 4. Monitor Progress

```bash
# Check overall status
haunted status

# List all issues
haunted issue list

# View specific issue details
haunted issue show <issue-id>

# View issues by status
haunted issue list --status in_progress
```

## Workflow

Haunted implements the development workflow from `docs/DEVELOPMENT_WORKFLOW.md`:

1. **Plan**: AI analyzes requirements and creates implementation strategy
2. **Implement**: AI writes code following the plan
3. **Unit Test**: AI creates and runs unit tests
4. **Fix Issues**: AI fixes any test failures
5. **Integration Test**: AI runs integration tests
6. **Diagnose**: If integration tests fail, AI diagnoses and replans
7. **Done**: Issue completed and merged

## Commands

### Core Commands

- `haunted init` - Initialize Haunted in current project
- `haunted start` - Start the AI daemon
- `haunted stop` - Stop the daemon
- `haunted status` - Show current status

### Issue Management

- `haunted issue create <title>` - Create new issue
- `haunted issue list` - List all issues
- `haunted issue show <id>` - Show issue details
- `haunted issue comment <id> <message>` - Add comment to issue

### Phase Management

- `haunted phase create <name>` - Create new phase
- `haunted phase list` - List all phases

## Configuration

Configuration is stored in `.haunted/config.json`:

```json
{
  "project": {
    "name": "your-project",
    "root": "/path/to/project"
  },
  "database": {
    "url": "/path/to/.haunted/database.db"
  },
  "claude": {
    "command": "claude",
    "maxTokens": 4000,
    "temperature": 0.7
  },
  "workflow": {
    "autoProcess": true,
    "checkInterval": 30000,
    "maxRetries": 3
  },
  "logging": {
    "level": "info"
  }
}
```

## Architecture

```
src/
├── cli/           # Command-line interface
├── commands/      # Individual command implementations
├── services/      # Core business logic
│   ├── claude-wrapper.ts # Claude Code CLI integration
│   ├── workflow-engine.ts # Workflow engine
│   ├── database.ts       # Database management
│   ├── git-manager.ts    # Git operations
│   └── daemon.ts         # Background service
├── models/        # TypeScript data models
├── mcp/           # MCP tools for Claude
└── utils/         # Utilities and config
```

## Development Workflow Integration

Haunted is designed to work with your existing development workflow:

1. **Create Issues** for features, bugs, or tasks
2. **Let AI work** - Haunted processes Issues autonomously
3. **Review Results** - Check AI's work in Git branches
4. **Provide Feedback** - Add comments to blocked Issues
5. **Merge & Deploy** - Completed Issues are auto-merged

## Git Branch Strategy

- **main**: Production branch
- **phase/<name>**: Phase branches for organizing work
- **issue/<id>**: Individual Issue branches
- Auto-merge: Issues -> Phases -> Main (when ready)

## MCP Tools

Claude has access to comprehensive tools:
- File operations (read, write, list)
- Command execution
- Git operations
- Issue management
- Code search and analysis

## Troubleshooting

### Common Issues

1. **Claude Code not authenticated**: Run `claude login` first
2. **Claude Code not installed**: Install from https://claude.ai/download
3. **Node.js version < 20**: Upgrade to Node.js 20 or higher
4. **Not a Git repository**: Run `git init` first
5. **Database errors**: Delete `.haunted/database.db` and reinitialize

### Logs

Enable verbose logging:
```bash
haunted --verbose start
```

Or specify log file:
```bash
haunted --log-file haunted.log start
```

## Examples

### Basic Workflow

```bash
# Initialize project
haunted init

# Create issues
haunted issue create "Add user model" --priority high
haunted issue create "Implement API endpoints" --priority high
haunted issue create "Add input validation" --priority medium

# Start AI processing
haunted start

# Monitor progress
watch haunted status
```

### Issue Management

```bash
# View issue details
haunted issue show abc123

# Add clarification comment
haunted issue comment abc123 "Please use bcrypt for password hashing"

# Check all open issues
haunted issue list --status open
```

## Contributing

1. Fork the repository
2. Create feature branch: `git checkout -b feature/name`
3. Make changes and test
4. Submit pull request

## License

MIT License - see LICENSE file for details.