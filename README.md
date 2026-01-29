# BlackBoard Skills

## What are Skills?

**Skills** are specialized capabilities that can be invoked by GitHub Copilot to perform specific tasks or respond to particular user inputs. Think of them as custom instructions that extend Copilot's functionality for your specific use cases.

Skills are stored in the `.github/skills/` directory and provide a way to create reusable, contextual responses that Copilot can leverage when working on your codebase.

## How Skills Work

When you interact with GitHub Copilot, it can recognize specific patterns or phrases and invoke the appropriate skill to provide a tailored response. Skills act as specialized agents that:

1. **Respond to specific triggers** - Like keywords or phrases (e.g., "rise")
2. **Provide consistent behavior** - Define how Copilot should respond in specific situations
3. **Encapsulate domain knowledge** - Store expertise about your project or workflows
4. **Enable custom workflows** - Create specialized responses for your team's needs

## Skill Structure

Each skill is defined in a `SKILL.md` file within its own directory under `.github/skills/`. The format is:

```markdown
---
name: SkillName
description: Brief description of what this skill does and when to use it.
---

## Detailed Instructions

Detailed instructions for how Copilot should use this skill...
```

### Components:

- **Frontmatter (YAML)**: Contains metadata
  - `name`: The unique identifier for the skill
  - `description`: A concise explanation of the skill's purpose and trigger conditions

- **Body**: Detailed instructions that tell Copilot:
  - When to activate this skill
  - What actions to perform
  - How to format the response
  - Any specific requirements or constraints

## Example: RiseAndShine Skill

Located at `.github/skills/RiseAndShine/SKILL.md`:

```markdown
---
name: RiseAndShine
description: This is a simple skill that should be used to respond to a user when they enter "rise".
---

## Rise and Shine

Use this Rise and Shine skill to respond to a user when they enter the phrase "rise".

respond with "Happy Coding" in ascii art.
```

When a user types "rise", Copilot recognizes this trigger and responds with ASCII art saying "Happy Coding".

## Creating a New Skill

To create a new skill:

1. Create a new directory under `.github/skills/` with your skill name
2. Create a `SKILL.md` file in that directory
3. Define the frontmatter with `name` and `description`
4. Write detailed instructions for how Copilot should use the skill

**Example structure:**
```
.github/
└── skills/
    └── YourSkillName/
        └── SKILL.md
```

## Best Practices

- **Clear descriptions**: Make the trigger conditions and purpose obvious
- **Specific instructions**: Be explicit about what the skill should do
- **Unique names**: Use descriptive, unique names for each skill
- **Focused scope**: Each skill should handle one specific task or response
- **Test your skills**: Verify that Copilot responds as expected

## Benefits of Using Skills

- **Consistency**: Ensure uniform responses across your team
- **Efficiency**: Automate common responses and workflows
- **Customization**: Tailor Copilot's behavior to your project's needs
- **Documentation**: Self-documenting patterns and workflows
- **Reusability**: Share skills across your organization

---

*Skills are a powerful way to extend GitHub Copilot's capabilities and make it more effective for your specific use cases.*
