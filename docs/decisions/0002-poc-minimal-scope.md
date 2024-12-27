# 0002 Dev bloom PoC minimal scope definition

| **Status:** Accepted | **Driver:** @pfouilloux |**Date:** 28-12-2024 |

## Executive summary

In the context of the initial proof of concept,
facing the need to define a minimal feature set,
we decided for implementing only core connectivity features
and against including additional capabilities.
This will achieve the quickest path to a working cross-platform prototype,
accepting limited container customization options initially.

## Context and problem statement

Following our decision to create a minimal proof of concept (0001-poc-approach), we need to define the smallest set of features that would:

- Prove technical feasibility
- Work on both Windows and Linux
- Offer actual utility to Visual Studio Code/Codium users
- Validate our core architectural approach

The challenge is identifying the features that are truly essential for a minimal working implementation compared to what can wait.

## Decision drivers

- Need for quick technical validation
- Visual studio code/Codium integration requirements
- Cross-platform compatibility
- Dev container spec compatibility
- Implementation complexity

## Considered options

- Option 1: Basic Container Connection Only
- Option 2: Container Connection + Basic Extensions Support
- Option 3: Container Connection + Volume Mounts
- Option 4: Container Connection + Volume Mounts + Basic Extensions

## Decision outcome

Chosen option: "Container Connection + Volume Mounts"

Rationale:

- Represents minimum viable feature set for development
- Covers core cross-platform challenges
- Allows validation of key technical approaches
- Provides clear user value
- Manageable implementation scope

### Essential features

1. Container Operations:
   - Container creation from basic Dockerfile
   - Start/stop container
   - Basic health monitoring

2. Volume Mounting:
   - Workspace folder mounting
   - User home directory mounting (for config)
   - Cross-platform path translation

3. Editor Integration:
   - Visual studio code/Codium remote connection protocol
   - Basic terminal access
   - File system access

### Explicitly excluded

1. Advanced Features:
   - Custom container configuration
   - Multi-container support
   - Network configuration
   - Extension preinstallation
   - Dev container features/templates

2. Container Management:
   - Container rebuild
   - Resource limits
   - Port forwarding
   - Environment customization

### Positive consequences

- Clear, focused development targets
- Faster path to first working prototype
- Simpler initial codebase
- Easier to validate cross-platform approach
- Core functionality for basic development workflow

### Negative consequences

- Limited container customization
- No advanced development features
- Manual setup required for many scenarios
- Not suitable for complex development environments

## Benefits and drawbacks of options

### Option 1: Basic container connection only

- Good, because simplest possible implementation
- Good, because fastest to implement
- Bad, because too limited for real development
- Bad, because does not validate volume mounting

### Option 2: Container connection + basic extensions support

- Good, because improves development experience
- Good, because validates extension architecture
- Bad, because adds complexity without core value
- Bad, because users can install extensions manually

### Option 3: Container connection + volume mounts

- Good, because covers essential development needs
- Good, because validates core cross-platform challenges
- Good, because provides clear user value
- Bad, because manual extension management
- Bad, because limited container customization

### Option 4: Container connection + volume mounts + basic extensions

- Good, because better development experience
- Good, because more complete feature set
- Bad, because increased initial complexity
- Bad, because longer implementation time
- Bad, because more potential issues to debug

## Links

- [Earlier decision: proof of concept approach](0001-poc-approach.md)
- [Dev Container Specification](https://containers.dev/)
