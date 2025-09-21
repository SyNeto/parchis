# Parchís Multiplayer Backend

A real-time multiplayer implementation of the classic Latin American board game Parchís (3-marble variant), built with Elixir/Phoenix using modern software engineering principles and AI-assisted development methodology.

## 🎯 Project Overview

This project demonstrates:
- **Clean Architecture**: Umbrella project with clear separation of concerns
- **AI-Assisted Development**: Systematic use of AI agents for development workflow
- **Modern Software Engineering**: Evidence-based practices from "Modern Software Engineering" book
- **Real-time Multiplayer**: Phoenix Channels for synchronous game state management

## 🎲 Game Rules

Traditional Parchís with 3 marbles per player:
- 2-4 players, each with 3 marbles
- Roll specific number (5 or 6) to exit home
- Move marbles around board in counter-clockwise direction
- Capture opponent marbles by landing on their position
- First player to get all 3 marbles to finish line wins

## 🏗️ Architecture

**Umbrella Project Structure:**
```
apps/
├── parchis_core/     # Pure game logic (no external dependencies)
├── parchis_game/     # Process management & state coordination  
└── parchis_web/      # Phoenix channels & HTTP interface
```

**Key Design Decisions:**
- **GenServer per Game**: Isolated game state management
- **Turn-based Synchronization**: Simple concurrency model
- **Connection Recovery**: Resilient to temporary disconnections
- **No Event Sourcing**: Current state only, no move history

## 📋 Architecture Decision Records (ADRs)

All architectural decisions are documented in `/docs/adr/`:

- [ADR-001](docs/adr/ADR-001-application-architecture.md): Application Architecture (Umbrella vs Single App)
- [ADR-002](docs/adr/ADR-002-game-state-managemente.md): Game State Management Pattern

## 🚀 Getting Started

(coming soon)



## 🤖 AI-Assisted Development

This project showcases systematic AI integration in software development:

1. **Architecture Planning**: ADRs designed with AI assistance
2. **Code Generation**: Focused AI agents for specific app layers
3. **Testing Strategy**: AI-generated property-based tests
4. **Documentation**: Automated documentation generation

### AI Workflow Example
```bash
# Context-focused development
# Only load relevant app when working on specific layer
cd apps/parchis_core  # Pure logic development
cd apps/parchis_game  # Process management
cd apps/parchis_web   # Client interface
```

## 📚 Learning Resources

- **Elixir/OTP**: "Elixir in Action" (Saša Jurić)
- **Phoenix Framework**: "Programming Phoenix 1.4" (Chris McCord)
- **Real-time Systems**: "Real-Time Phoenix" (Stephen Bussey)
- **Modern Engineering**: "Modern Software Engineering" (David Farley)

## 🧪 Testing Philosophy

- **Pure Functions First**: Core game logic is fully deterministic
- **Property-Based Testing**: Game rules validated with extensive edge cases
- **Integration Testing**: Full game flow validation
- **Fast Feedback**: Isolated unit tests for rapid iteration

## 🔄 Documentation Status

- [x] Architecture design and ADR documentation
- [x] Umbrella project structure
- [ ] Core game logic implementation
- [ ] GenServer game state management
- [ ] Phoenix channels real-time communication
- [ ] Web client interface
- [ ] Performance testing and optimization

## 🤝 Contributing

This is primarily a learning and methodology demonstration project. However, contributions that align with the AI-assisted development approach are welcome.

Please read the ADRs in `/docs/adr/` to understand architectural decisions before contributing.

