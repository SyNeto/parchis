# Parchís Multiplayer Backend

A real-time multiplayer implementation of the classic Latin American board game Parchís (3-marble variant), built with Elixir/Phoenix using modern software engineering principles and AI-assisted development methodology.

## 🎯 Project Overview

This project demonstrates:
- **Clean Architecture**: Umbrella project with clear separation of concerns
- **AI-Assisted Development**: Systematic use of AI agents for development workflow
- **Modern Software Engineering**: Evidence-based practices from "Modern Software Engineering" book
- **ADR-Driven Design**: All architectural decisions documented before implementation

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
- **Strategy Pattern**: Flexible game variant support with clean interfaces
- **Turn-based Synchronization**: Simple concurrency model
- **Connection Recovery**: Resilient to temporary disconnections
- **No Event Sourcing**: Current state only, no move history

## 📋 Architecture Decision Records (ADRs)

All architectural decisions are documented in `/docs/adr/`:

### ✅ Completed
- [ADR-001](docs/adr/ADR-001-application-architecture.md): Application Architecture (Umbrella vs Single App)
- [ADR-002](docs/adr/ADR-002-game-state-managemente.md): Game State Management Pattern
- [ADR-004](docs/adr/ADR-004-business-logic): Business Logic Separation

### 🔄 In Progress
- [ADR-003](docs/adr/003-client-server-communication.md): Client-Server Communication Protocol *(next)*

### 📋 Planned
- ADR-006: Concurrency and Race Conditions Management
- ADR-007: Supervision and Fault Tolerance Strategy
- ADR-008: Testing Strategy
- ADR-005: Persistence Strategy
- ADR-009: Observability and Monitoring
- ADR-010: Deployment and Release Strategy

## 🤖 AI-Assisted Development

This project showcases systematic AI integration in software development:

1. **Architecture Planning**: ADRs designed with AI assistance for evidence-based decisions
2. **Context-Focused Development**: AI agents work on specific app layers to maintain clean context
3. **Interface-First Design**: Strategy pattern enables clean public contracts
4. **Documentation-Driven**: All decisions documented before implementation

### AI Workflow Example
```bash
# Context-focused development
# Only load relevant app when working on specific layer
cd apps/parchis_core  # Pure logic development
cd apps/parchis_game  # Process management
cd apps/parchis_web   # Client interface
```

## 📚 Learning Resources

Key references used in architectural decisions:
- **Elixir/OTP**: "Elixir in Action" (Saša Jurić)
- **Phoenix Framework**: "Programming Phoenix 1.4" (Chris McCord)
- **Real-time Systems**: "Real-Time Phoenix" (Stephen Bussey)
- **Modern Engineering**: "Modern Software Engineering" (David Farley)
- **Functional Design**: "Domain Modeling Made Functional" (Scott Wlaschin)

## 🧪 Development Philosophy

- **Evidence-Based Decisions**: All architectural choices backed by research and documented reasoning
- **Fast Feedback**: Clean boundaries enable isolated testing and development
- **Strategy-First**: Public interfaces hide complexity and enable flexibility
- **Pragmatic Scope**: Start with 3-marble basic variant, evolve incrementally

## 🔄 Development Status

### Architecture Phase
- [x] Core architectural decisions documented in ADRs
- [x] Umbrella project structure defined
- [x] Game state management strategy decided
- [x] Business logic separation pattern established
- [ ] Client-server communication protocol *(in progress)*
- [ ] Remaining infrastructure ADRs

### Implementation Phase *(not started)*
- [ ] Core game logic implementation
- [ ] GenServer game state management
- [ ] Phoenix channels real-time communication
- [ ] Web client interface
- [ ] Testing suite development

## 📁 Repository Structure

```
/
├── docs/adr/                 # Architecture Decision Records
├── README.md                 # This file
└── (implementation files will be added after ADR completion)
```

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🤝 Contributing

This is primarily a learning and methodology demonstration project. The focus is on showcasing AI-assisted development principles and modern software engineering practices.

Please read the ADRs in `/docs/adr/` to understand architectural decisions before contributing.

---

*Built with ❤️ using AI-assisted development principles and modern software engineering practices.*
