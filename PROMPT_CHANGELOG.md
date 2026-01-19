# Prompt Version Changelog

This document tracks changes to the agent system prompts in `tsg_constants.py`.

## Version 1.1 (2026-01-19)

**Comprehensive Prompt Improvements**

Major enhancements to all three agent prompts with detailed instructions, examples, and quality guidelines.

### Researcher Agent
- Extensive role and objective documentation
- Detailed relevance decision tree for source evaluation
- Priority-based research process (user URLs first, official docs second, community third)
- GitHub deep-dive instructions with workaround extraction
- Step-by-step research process with validation checklist
- Self-check quality criteria before output
- Enhanced output format with structured sections

### Writer Agent
- Comprehensive section-specific instructions
- Clear decision tree for placeholder usage
- Explicit fabrication rules and examples
- Detailed Related Information relevance filter
- Step-by-step writing process with validation
- Enhanced quality self-check with multiple dimensions
- Clearer distinction between internal and customer-facing content

### Reviewer Agent
- Detailed 7-step review process
- Five-dimension validation framework (structure, accuracy, relevance, completeness, format)
- Auto-correction decision tree and guidelines
- Common review scenarios with examples
- Strictness guidelines for consistent quality
- Enhanced output format with detailed issue categorization
- Clearer guidance on when corrections are auto-fixable

### Breaking Changes
- None - prompts remain compatible with existing workflow

---

## Version 1.0 (Pre-2026-01-19)

**Initial Baseline**

Original prompt versions before comprehensive improvements. Included basic instructions for the three-agent pipeline.

### Characteristics
- Concise agent instructions
- Basic research and writing guidelines
- Simple review criteria
- Functional but less detailed

---

## Version Numbering Guidelines

- **MAJOR (X.0)**: Breaking changes to prompt structure or behavior requiring agent recreation
- **MINOR (X.Y)**: Compatible improvements, clarifications, and bug fixes

When updating prompts:
1. Update `PROMPT_VERSION` in `tsg_constants.py`
2. Add entry to this changelog describing changes
3. Commit changes to git
4. Users will be notified in the web UI (setup section) to recreate agents
