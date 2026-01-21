
## **Title:** 
**AI as Glue Using MCP: Deterministic Output in a Non-Deterministic Sandbox**

## **Abstract:**

LLMs are probabilistic by nature—they hallucinate, they drift, they can't be trusted with critical decisions alone. Yet engineering workflows are full of gaps that desperately need filling: extracting values from webhook payloads, transforming API responses, routing decisions between tools. These are tasks where AI's flexibility is exactly what we need, but only if we can constrain the chaos.

This is where MCP changes the game. By wrapping deterministic tools—CLIs, APIs, databases—in a protocol that AI can reliably interface with, we get the best of both worlds: AI handles the messy transformation layer while battle-tested tools handle the actual operations.

This talk explores the practical architecture of "AI as glue" using MCP:

**The Limitations We're Working With:**
- LLMs can't be trusted to execute critical operations directly
- Prompt injection and hallucination are real production risks
- Non-deterministic systems require deterministic boundaries

**How MCP Provides the Guardrails:**
- Structured tool definitions give AI reliable interfaces, not open-ended access
- Read/write separation lets AI analyze without modifying
- Deterministic tools (GitHub CLI, test runners, Snyk API) do the actual work
- AI fills the gaps: condensing context, extracting values, deciding which tool to call next

Through real production examples—automated security patching, build failure triage, repository maintenance—you'll see patterns for composing workflows where AI orchestrates but never operates alone. Each step has a deterministic tool at its core, with AI serving as the connective tissue that was previously written in brittle bash scripts or abandoned as "too complex to automate."

The rougher your tool interfaces, the more texture there is for the glue to grab onto. MCP makes that texture programmable.
