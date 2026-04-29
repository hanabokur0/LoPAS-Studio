# LoPAS Studio

A visual protocol architecture builder.  
Drag protocols onto a canvas, connect them by socket type, and watch learning loops emerge.

Build AI + human workflows like molecular systems.
Connect protocols.
Detect learning loops.
Deploy real-world decision systems.
---

## What it does

LoPAS Studio treats protocols and skills as **molecules**.  
Each one has typed sockets — inputs on the left, outputs on the right.  
You connect them like chemical bonds: only matching types can link.

When your connections form a cycle, the system detects it  
and tells you: **Learning Spiral Detected**.

That's the difference between a pipeline and a living system.

---

## Socket Types

Every protocol communicates through six data types:

| Socket | Label | Description |
|--------|-------|-------------|
| `observation` | OBS | Raw observed data |
| `question` | QST | A structured question |
| `judgment` | JDG | A decision or classification |
| `action` | ACT | An executable step |
| `context` | CTX | Situational framing |
| `feedback` | FBK | Return signal from outcomes |

A connection is valid only when the output type of one protocol  
matches the input type of another.

---

## Built-in Protocols

### Thinking

| Protocol | Sockets | Description |
|----------|---------|-------------|
| **Observation Before Opinion** (OBO) | → OBS | Observe facts before forming opinions |
| **Concept Stress-Test** (CST) | OBS, QST → JDG | Generate structural counterarguments |
| **Question Cultivation** (QCP) | OBS, FBK → QST | Grow questions that produce structural change |

### Business

| Protocol | Sockets | Description |
|----------|---------|-------------|
| **Meeting Decision** (MTD) | CTX, OBS → JDG, ACT | Structure meeting decisions |

### AI

| Protocol | Sockets | Description |
|----------|---------|-------------|
| **Session Initialization** (SIN) | CTX → ACT, CTX | Structure AI session context |

### Framework

| Protocol | Sockets | Description |
|----------|---------|-------------|
| **RNC Validator** (RNC) | JDG, ACT → JDG, FBK | Validate through Responsibility Normalization Contract |
| **LoPAS MCCP** (MCP) | OBS, FBK → CTX, OBS | Memory Compression & Classification Protocol |
| **CAG Core** (CAG) | OBS → OBS, JDG | Measure Cognitive-Action Gap |

### Learning

| Protocol | Sockets | Description |
|----------|---------|-------------|
| **LCA Classifier** (LCP) | OBS, FBK → JDG, CTX | Classify whether learning occurred |
| **LCA Validation** (LCV) | JDG → FBK, OBS | Validate learning claims by structural change |
| **Unknown Retention** (UNR) | FBK → OBS, CTX | Hold unresolved structure for re-observation |

---

## Add Your Own Protocol

Click **+ Add Protocol** in the sidebar.  
Write in Markdown or Python dict format.

### Markdown

```markdown
# Error Classifier
shortname: ERC
category: Operations
description: Classify errors by structural pattern
inputs: observation
outputs: judgment, context
```

### Python

```python
{
  "name": "Error Classifier",
  "short_name": "ERC",
  "category": "Operations",
  "desc": "Classify errors by structural pattern",
  "inputs": ["observation"],
  "outputs": ["judgment", "context"]
}
```

The parser reads your definition, validates socket types,  
and adds it to the library. Drag it onto the canvas and connect.

---

## How It Works

```
Library          Canvas              Detection
┌──────────┐    ┌────────────────┐   ┌───────────┐
│ Protocol │───>│ Drag & Place   │   │           │
│ Protocol │    │ Connect Sockets│──>│ Loop?     │
│ Protocol │    │ Build Flow     │   │  → Spiral │
│ + Add    │    │                │   │  → Linear │
└──────────┘    └────────────────┘   └───────────┘
```

1. **Drag** a protocol from the library onto the canvas
2. **Connect** output sockets to input sockets of the same type
3. **Observe** — if the graph forms a cycle, the system detects a Learning Spiral
4. **Add** your own protocols in Markdown or Python
5. **Iterate** — restructure, reconnect, test different architectures

---

## Design Principle

Most automation tools chain actions in a line:

```
input → process → output
```

LoPAS Studio builds architectures that loop:

```
observation → judgment → action → feedback → observation
```

The six socket types are not arbitrary.  
They represent the minimum vocabulary for describing  
how decisions flow through any system — human, AI, or hybrid.

---

## Related

- [LoPAS-LCA](https://github.com/hanabokur0/LoPAS-LCA) — Learning Claim Architecture
- [Skill Library](https://github.com/hanabokur0/skill-library) — Markdown skills for any AI
- [Shikou Tree](https://github.com/hanabokur0/shikou_tree) — Thought tree visualization
- [LoPAS-MCCP](https://github.com/hanabokur0/LoPAS-MCCP) — Memory Compression & Classification Protocol
- [LoPAS-Core](https://github.com/hanabokur0/LoPAS-Core) — The observation framework

---

## License

MIT

## Author

花黒子 (Hanabokur0)
