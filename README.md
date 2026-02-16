# Claude PM Skills Library

Custom AI skills that encode product management best practices into reusable automation. Built to reduce routine PM work and scale domain expertise across teams. Also it will allow for better + structured prompting while AI will ask you clarifying questions where applicable to ensure it challenges your thinking and exposes weak spots (crucial for a strategic role such as Product Management).
Purpose is Skill -> feeds a Project and Instructions -> prepare AI to function within the Project's scope and context. That's where you can derive the biggest value from and avoid any hallucinations of sorts.

## Overview

This repository contains production-ready Claude AI skills designed for product managers working in ticketing, payments, and multi-market environments. Each skill transforms hours of manual work into seconds of automated output while maintaining quality and consistency.

## Why These Skills Exist

**The Problem:**
- PRD creation takes 2-4 hours of structured writing
- Roadmap updates require manual synthesis across multiple sources
- Stakeholder communications consume 5+ hours weekly
- Quality varies based on PM experience level
- Domain knowledge doesn't scale beyond individuals

**The Solution:**
Custom AI skills that:
- Encode 10+ years of product expertise into reusable prompts
- Apply consistent structure and quality standards
- Generate first drafts in seconds instead of hours
- Scale best practices across junior and senior PMs alike
- Free up time for strategic thinking and customer engagement

## Sample Skills Included

### 1. PRD Generator
**Purpose:** Transforms rough discovery notes into structured Product Requirement Documents

**Input:** Meeting transcripts, customer interviews, brainstorming notes, strategy docs

**Output:** Complete PRD with:
- Executive Summary (problem, solution, business case)
- Success Metrics (measurable KPIs with targets)
- Assumptions (testable hypotheses)
- Scope & Requirements (in/out of scope by market)
- User Journeys (JTBD format)
- Technical Considerations (APIs, architecture, performance)
- Open Questions (with owners and tracking)
- Edge Cases (error scenarios, failure modes)
- Security & Privacy (compliance by market)
- Dependencies (blockers, prerequisites)
- Timeline (phases and milestones)

**Time Saved:** 2-4 hours → 15 minutes (including review/editing)

**Quality Improvement:** Consistent 90+ score on PRD Completeness Validator

**Key Features:**
- Market-specific compliance (UK: FCA/PSD2, EU: GDPR, US: state regulations)
- Technical pattern recognition (payment → PCI, data → privacy assessment)
- Metric templating by product type (e-commerce, SaaS, marketplace)
- Gap detection and intelligent questioning

---


**60+ Use Cases:**
- Quarterly planning sessions
- Board/investor updates
- Team alignment meetings
- Strategy documentation
- More

---


## Technical Architecture

### Skill Structure
Each skill follows Claude's skill architecture:

```
skill-name/
└── SKILL.md
    ├── Purpose
    ├── When to Use
    ├── Core Capabilities
    ├── Input Formats
    ├── Output Format
    ├── Intelligent Behavior
    ├── Quality Standards
    └── Success Indicators
```

### Design Principles

**1. Domain Encoding**
Skills embed real PM expertise:
- 10 years across ticketing, payments, fintech, FMCG, eCommerce
- Multi-market operations (UK, EU, US, 10+ countries)
- Compliance knowledge (PCI DSS, GDPR, PSD2, FCA regulations)
- Technical fluency (APIs, system design, data pipelines)

**2. Quality Gates**
Built-in validation:
- Completeness checks (no missing critical sections)
- Metric specificity (no vague "improve experience")
- Testable assumptions (falsifiable hypotheses)
- Edge case coverage (failure modes documented)

**3. Context Awareness**
Adapts to:
- Product type (B2B/B2C, marketplace, SaaS, infrastructure)
- Market (different compliance by region)
- Stage (concept vs detailed spec)
- Audience (engineering, exec, cross-functional)

## Installation & Usage

### Adding to Claude Projects

1. **In Claude.ai:**
   - Navigate to your Project (e.g., "Planning & Delivery")
   - Click Settings → Skills
   - Click "Add Custom Skill"
   - Upload the relevant `SKILL.md` file

2. **Test the skill:**
   ```
   [Provide your input - notes, docs, data]
   
   Generate a PRD / roadmap / update based on this.
   ```

3. **Review and refine:**
   Claude generates a first draft following the skill template.
   Edit as needed for your specific context.

### GitHub Integration

Clone this repo to access skills locally:

```bash
git clone https://github.com/dimospapadopoulos/claude-pm-skills.git
cd claude-pm-skills
```

Upload skills to Claude Projects via web interface or API.

## Real-World Impact

### Productivity Gains
- **Document creation time:** 60% reduction (15+ hours saved weekly)
- **PRD quality score:** Consistent 90+ on validation (vs 60-75 manual)
- **Review cycles:** 40% reduction (fewer clarifying questions from eng)
- **Stakeholder prep time:** 75% reduction (10 minutes vs 1 hour)

### Team Scaling
- Junior PMs produce senior-quality specs from day 1
- Consistent standards across 10+ market requirements
- Institutional knowledge encoded (survives team turnover)
- Onboarding time reduced by 50% (learn by example)

### Strategic Impact
- Time freed up for customer discovery (+5 hours/week)
- Faster iteration (specs done in hours, not days)
- Better decision quality (consistent frameworks applied)
- Reduced engineering blockers (clearer, more complete specs)

## Integration with Other Tools

**Works seamlessly with:**
- [PRD Completeness Validator](https://github.com/dimospapadopoulos/prd-completeness-validator) - Validates generated PRDs
- [Voice of Customer Synthesizer](https://github.com/dimospapadopoulos/voc-portfolio-clean) - Feeds customer insights into PRDs
- Claude Projects ecosystem (Strategy, Delivery, Research, Analytics, Communications, Technical specs)
- Slack (via bot integration for on-demand generation)
- Google Docs (import/export for collaboration)

## Customization Guide

### Adapting for Your Domain

1. **Edit templates in SKILL.md:**
   - Update section headings to match your org's PRD template
   - Modify success metrics for your product type
   - Add industry-specific compliance requirements

2. **Adjust quality standards:**
   - Change passing score threshold (default: 90/100)
   - Weight sections by importance (critical/high/medium)
   - Add custom validation rules

3. **Extend capabilities:**
   - Add market-specific templates
   - Include your org's terminology
   - Embed your strategic frameworks (RICE, AARRR, etc.)

### Example Customizations

**For SaaS Companies:**
- Add activation/retention metrics
- Include feature adoption tracking
- Emphasize integration requirements

**For E-commerce:**
- Focus on conversion funnel metrics
- Add payment method considerations
- Include fraud prevention requirements

**For B2B:**
- Enterprise security requirements
- Multi-tenant considerations
- SLA and compliance sections

## What I Learned Building This

**Product Thinking:**
- Codifying "good PM work" requires deep domain expertise
- Skills improve through iteration based on real usage
- Quality automation scales expertise better than documentation
- Best practices are contextual (no one-size-fits-all)

**Technical Skills:**
- Prompt engineering at production scale
- Structured output generation (YAML, markdown, tables)
- Context management (what to include, what to omit)
- Skill composition (how skills reference each other)

**Team Enablement:**
- Tools that encode judgment create consistent quality
- Fast feedback loops accelerate learning
- Automation doesn't replace thinking / it gave me more time to think through systems/architecture.
- Junior PMs learn by seeing examples, not just reading docs. Gone are the days I searched on Google and libraries to complete my thesis: "Electrical Treeing as a Result of Mechanical Stresses" in 2017.

## Roadmap

### V1.1 (Next 30 Days)
- [ ] Add metric calculation examples
- [ ] Include PRD templates by product type (feature, API, infrastructure)
- [ ] Enhance market-specific compliance rules

### V2.0 (Q2 2026)
- [ ] Slack bot integration (`/generate-prd`, `/create-roadmap`, `/status-update`)
- [ ] Google Docs import/export
- [ ] Version control and change tracking
- [ ] Team collaboration features

### V3.0 (Q3 2026)
- [ ] AI-powered PRD review and suggestions
- [ ] Automated roadmap optimization
- [ ] Predictive analytics (estimate completion times)
- [ ] Integration with project management tools (Jira, Linear)

## Contributing

This is a personal productivity library, but if you want to adapt these skills for your org:

1. Fork the repository
2. Customize SKILL.md files for your domain
3. Test thoroughly with your team's real work
4. Share learnings (optional - via issues/discussions) - reach out to me via Git or LI or email (portfolio linked below)

## License

This project is licensed under the BSD 3-Clause License; please attribute [Dimos Papadopoulos/Claude PM skills] in all redistributions or derived works.

---

## About

**Author:** Dimos Papadopoulos  
**Role:** Product Manager
**Domain:** Ticketing, Payments, Multi-Market Product Development, eCommerce  
**Background:** 10 years across entertainment, electronics, FMCG, eCommerce, fashion

**Why I Built This:**
As a PM moving to leadership roles, I needed to:
1. Scale my output without sacrificing quality
2. Encode domain expertise so it survives any job changes
3. Demonstrate technical capability (not just talk about it)
4. Free up time for strategic work vs document creation

These skills save me 15+ hours weekly and produce consistently high-quality output. They're the automation I wish I had when I started out my career in 2017.

**Connect:**
- GitHub: [@dimospapadopoulos](https://github.com/dimospapadopoulos)
- LinkedIn: [Dimos Papadopoulos](https://linkedin.com/in/dimosp)
- Portfolio: [Other Projects](https://www.notion.so/Dimos-Papadopoulos-Product-Portfolio-ad6dd941f79c4d28bfc741db4ea6be95)

## Related Projects

- **[PRD Completeness Validator](https://github.com/dimospapadopoulos/prd-completeness-validator)** - Validates PRDs against quality standards (pairs with PRD Generator skill directly into your Projects - as you automate 60% of your time towards more strategic thinking)
- **[Voice of Customer Synthesizer](https://github.com/dimospapadopoulos/voc-portfolio-clean)** - Analyzes 150k+ feedback entries annually (feeds insights into Slack for actionability)

---

**Built with:** Claude AI, 10 years of PM experience, and a belief that good automation scales expertise / not replacing it!

**Last Updated:** February 2026