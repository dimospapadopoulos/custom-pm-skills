# PRD Generator Skill

## Purpose
Transforms rough discovery notes, meeting transcripts, or brainstorming sessions into structured Product Requirement Documents following enterprise best practices.

## When to Use This Skill
- User provides meeting notes, research findings, or unstructured ideas
- User says "turn this into a PRD" or "help me write a spec"
- User shares problem statements that need formal documentation
- User references customer feedback requiring product response

## Core Capabilities

### 1. Structure Recognition
Extracts key elements from unstructured input:
- Problem statements and pain points
- User needs and jobs-to-be-done
- Business objectives and success criteria
- Technical constraints and dependencies
- Market requirements and compliance needs

### 2. Template Application
Applies consistent PRD structure:
- Executive Summary (problem, solution, business case)
- Success Metrics (KPIs, targets, measurement approach)
- Assumptions (what we believe to be true)
- Scope & Requirements (in scope, out of scope, by market/phase)
- User Journeys (as a/I want/so that format)
- Technical Considerations (APIs, architecture, performance)
- Open Questions (what needs clarification)
- Edge Cases (error scenarios, failure modes)
- Security & Privacy (compliance, data protection)
- Dependencies (blockers, prerequisites)
- Timeline (milestones, phases)

### 3. Content Enhancement
- Fills gaps with industry best practices
- Suggests metrics based on problem type
- Identifies implied requirements
- Flags missing critical sections
- Proposes edge cases to consider

## Input Formats Accepted
- Meeting transcripts
- Bullet-point notes
- Customer interview summaries
- Competitive analysis findings
- Strategy documents
- Slack thread exports
- Email chains

## Output Format

```markdown
# [Feature Name]

## Executive Summary
**Problem Statement:**
[Clear articulation of user pain point]

**Business Case:**
[Why this matters - revenue, retention, market positioning]

**Solution:**
[High-level approach]

**Value Proposition:**
[Benefits to users and business]

## Success Metrics
[Specific, measurable KPIs with targets and timeframes]

## Assumptions
[What we're assuming to be true - user behavior, technical feasibility, market conditions]

## Scope & Requirements
### In Scope - Phase 1
[Table format with capability, market, release, priority]

### Out of Scope
[What we're explicitly not doing and why]

## User Journeys
[As a... I want... So that... format with flows]

## Technical Considerations
[Architecture, APIs, performance requirements, system design]

## Open Questions
[Table with Question, Owner, Date Asked, Status, Notes]

## Edge Cases
[Error scenarios, failure modes, unusual conditions]

## Security & Privacy
[GDPR, PCI, compliance requirements]

## Dependencies
[What needs to happen first, blockers, prerequisites]

## Timeline
[Key milestones and phases]
```

## Intelligent Behavior

### Gap Filling
When input lacks detail, skill:
- Asks clarifying questions about missing critical sections
- Suggests standard approaches for common product types
- Provides examples to help user fill gaps

### Context Awareness
Adapts based on:
- Product type (B2B vs B2C, marketplace, SaaS, etc.)
- Market (US, UK, EU - different compliance needs)
- Stage (early concept vs detailed spec)
- Audience (engineering, exec, cross-functional)

### Quality Gates
Before presenting draft:
- Validates all critical sections present
- Checks metric specificity (no vague "improve experience")
- Ensures assumptions are testable
- Confirms edge cases cover failure modes

## Example Usage

### Input:
```
Meeting notes from customer interviews:
- 15 customers mentioned checkout is confusing
- Takes 3+ minutes to complete purchase
- Mobile users struggling more than desktop
- Abandonment rate is 32% 
- Want to add Apple Pay
- Legal approved UK market only
- Engineering says 2 sprints
```

### Output:
```markdown
# Apple Pay Integration - UK Market

## Executive Summary
**Problem Statement:**
Customers abandon checkout due to friction in payment entry. 
Current checkout averages 3+ minutes, with 32% abandonment rate. 
Mobile users particularly affected.

**Business Case:**
£2.3M annual revenue at risk from cart abandonment. Apple Pay 
adoption can reduce checkout time to <30 seconds, targeting 
40% reduction in abandonment.

[continues with full PRD structure...]
```

## Advanced Features

### Market-Specific Requirements
Automatically includes compliance considerations:
- UK: FCA, PSD2, PSRs
- EU: GDPR, PSD2, SCA requirements
- US: State-specific regulations (CCPA, etc.)

### Technical Pattern Recognition
Identifies common patterns:
- Payment integration → PCI compliance required
- User data → Privacy impact assessment needed
- Multi-market → Localization requirements
- API integration → Rate limiting, error handling

### Success Metric Templating
Suggests appropriate metrics by product type:
- E-commerce: Conversion rate, AOV, cart abandonment
- SaaS: Activation rate, feature adoption, retention
- Marketplace: GMV, take rate, liquidity
- Infrastructure: Latency, uptime, error rate

## Quality Standards

### Must Include:
- Measurable success metrics (not "improve UX")
- Specific scope boundaries (with rationale for out-of-scope)
- Testable assumptions
- Named owners for open questions
- Severity-tagged edge cases
- Compliance requirements by market

### Must Avoid:
- Vague success criteria ("better experience")
- Solution disguised as requirements
- Assuming technical approach without validation
- Missing security/privacy considerations
- Unrealistic timelines without dependencies mapped

## Skill Maintenance

### Version History
- v1.0: Initial release - core PRD structure
- v1.1: Added market-specific compliance templates
- v1.2: Enhanced technical pattern recognition
- v1.3: Improved metric suggestion engine

### Continuous Improvement
Skill improves through:
- Analysis of PRDs that led to successful launches
- Feedback from engineering on clarity/completeness
- Tracking which sections most often require rework
- Incorporating new regulatory requirements

## Success Indicators
Skill is working well when:
- Generated PRDs pass validation without major gaps
- Engineering asks fewer clarifying questions
- Product reviews take <15 minutes (vs 30+ previously)
- Junior PMs use output as learning examples
- Specs consistently include edge cases found in production

## Related Skills
- `prd-validator` - Validates generated PRDs against template
- `roadmap-generator` - Creates roadmaps from approved PRDs
- `stakeholder-update` - Generates status updates from PRD progress

---

**Skill Author:** Dimos Papadopoulos  
**Role:** Senior Product Manager  
**Domain Expertise:** Ticketing, Payments, Multi-Market Product Development  
**Created:** February 2026  
**Last Updated:** February 2026
