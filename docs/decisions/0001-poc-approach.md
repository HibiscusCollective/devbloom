# 0001 DevBloom PoC implementation approach

| **Status:** Accepted | **Driver:** @pfouilloux | **Date:** 27-12-2024 |

## Executive summary

In the context of the dev containers specification,
facing the need for Windows container support,
we decided for a  proof of concept of core devcontainer features
and against a full implementation.
This will achieve quick validation of our core technical approach,
accepting limited initial features and a delayed release.

## Context and problem statement

Development containers have become essential for consistent development environments, but current implementations:

- Rely heavily on Microsoft's proprietary technology
- Have limited Windows container support
- Create vendor lock-in concerns

We need to validate that we can create a viable alternative that:

- Works without Microsoft dependencies
- Supports both Windows and Linux containers
- Maintains compatibility with existing dev container specifications
- Provides a clear migration path for existing users

## Decision drivers

- Needs to work on codium based editors.
- Requirement for cross-platform container support
- Compatibility with existing dev container workflows
- Technical feasibility validation
- Community adoption potential

## Considered options

- Option 1: Full Feature Initial Implementation
- Option 2: Minimal proof of concept with core features
- Option 3: Windows-First Implementation
- Option 4: Linux-First Implementation

## Decision outcome

Chosen option: "Minimal proof of concept with core features"

Rationale:

- Allows fastest validation of core technical approach
- Reduces initial complexity
- Provides clear foundation for iterative development
- Enables early community feedback
- Validates both Windows and Linux support simultaneously

### Positive consequences

- Quick validation of technical approach
- Early feedback opportunity
- Clear focus for initial development
- Manageable scope
- Faster time to first usable version

### Negative consequences

- Limited initial functionality
- Might not immediately attract production users
- Could miss early feature requirements
- Initial version might not be practically useful

## Benefits and drawbacks of options

### Option 1: Full featured initial implementation

- Good, because provides complete solution from start
- Good, because matches existing tools' functionality
- Bad, because significantly delays first release
- Bad, because increases risk of architectural mistakes
- Bad, because reduces ability to incorporate early feedback

### Option 2: Minimal PoC with core features

- Good, because validates core technical approach quickly
- Good, because allows early community involvement
- Good, because reduces initial development complexity
- Bad, because limited initial functionality
- Bad, because might not be immediately useful in production

### Option 3: Windows-first implementation

- Good, because focuses on underserved market
- Good, because differentiates from existing solutions
- Bad, because delays Linux support
- Bad, because smaller initial user base
- Bad, because might miss Linux-specific requirements

### Option 4: Linux-first implementation

- Good, because targets larger developer base
- Good, because simpler initial implementation
- Bad, because delays Windows support
- Bad, because does not target key differentiation early
- Bad, because might complicate later Windows support

## Links

- [Project README](../../README.md)
- [Dev Container Specification](https://containers.dev/)
