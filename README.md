# Design System AI Ruleset

## Primary Steps

This design system follows a structured 4-phase workflow for creating components:

### 1. **Figma Connection Validation (MANDATORY)**
- Verify Figma design access and node ID availability
- **STOP IMMEDIATELY if design is not accessible**
- Document access status before proceeding

### 2. **Reuse vs Novel Component Assessment**
- Search existing components systematically
- Determine if component can be built from existing patterns
- If reuse: create delta plan; if novel: proceed to complexity assessment

### 3. **Complexity Assessment (for Novel Components)**
- Score component complexity (behavior, UI, data/logic)
- 0 characteristics: build custom
- 1-2 characteristics: check Radix UI
- 3+ characteristics: MUST use Radix primitive or document exception

### 4. **Figma Data Extraction & Architecture**
- Extract layout, spacing, states, and tokens from Figma
- Validate ALL tokens before use (never invent tokens)
- Plan component API, variants, and Storybook structure
- Document token gaps and architectural decisions

### 5. **Implementation**
- Use semantic tokens only (no primitives, no raw values)
- Implement layout with flexible sizing (no hard-coded dimensions)
- Add accessibility (focus ring, keyboard navigation, ARIA)
- Create comprehensive Storybook stories with autodocs
- Follow export pattern (default in file, named in index, root re-export)

### 6. **Definition of Done**
- All linting passes with 0 warnings
- Figma extraction complete and mapped to tokens
- Stories include autodocs, controls, and Figma link
- Component follows export pattern with ref forwarding
- Accessibility requirements met (focus ring, keyboard, contrast)

## Recommended Prompt

> It's time to make a component. First, read through the entire design system rules to understand the nuance. After reading through the rules, follow them and create this component: [add figma link]