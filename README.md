# design_system_ai_ruleset
A public repository to share rule sets used to build components with AI

Here's a summary of the MileIQ ruleset
gates:
  - Make sure AI can see Figma file, otherwise it will make stuff up
  - Lint the code
rules:
  - Use semantic tokens
  - Don't make hardcoded colors, type, space, etec
  - If complex enough, use Radix as scaffolding for the component
  - Accessibility checks
  - Export to other components any new component so we can reuse existing components
guidelines:
  - Use Material UI as an API reference
