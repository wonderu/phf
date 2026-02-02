# Project Handover Framework / Checklist

A checklist for taking over a project from the previous project manager.

## Table of contents

- [Description](#description)
- [How to use](#how-to-use)
- [Using AI to gather checklist data](AI-GATHERING.md)
- [Communications checklist](COMMUNICATIONS.md) (standups, statuses, retros, inside/outside)
- [What to handover?](#what-to-handover) (1. Product/Project Overview … 15. Handover sign-off)
- [What to read?](#what-to-read)
- [Contributing / Feedback](#contributing--feedback)
- [License](#license)

## Description

Checklist for taking over a project from the previous project manager. For incoming PMs, outgoing PMs, and team leads. Keep this information in one place and start collecting it from day one. Using this checklist reduces risk and rework during PM transitions.

## How to use

- Use this document as a checklist when taking over a project (tick off items as you go).
- Copy the checklist into your project wiki or handover doc and adapt as needed.
- Optionally track progress in a GitHub issue or task list.
- See [AI-GATHERING.md](AI-GATHERING.md) for recommendations on using AI to gather checklist data.
- If you're leaving: update this checklist with current state, schedule handover meetings, and hand off access and contacts by [date].

## What to handover?

- [ ] 1. Product/Project Overview

	- Functional and non-functional requirements
	- Use Cases
	- Business context, success criteria, scope boundaries, KPIs
	- Development metrics (e.g. velocity, cycle time, defect rate, burndown)
	- Pending work and deadlines (current tasks, upcoming milestones, overdue items, commitments)
  
- [ ] 2. Team
 
	- List of team members, org chart
	- **Outstaff vs in-house**: who is employed in-house vs outstaff/contractor; which vendor or agency each outstaff member comes from; different reporting lines, access provisioning, and escalation for each
	- **Team contact details**: emails (work), mobiles (work and private, where shared), Telegram (or other messengers) — who prefers which channel, who is on-call
	- Key contacts and escalation (stakeholders, tech lead, DevOps, security, vendors)
	- Key decision makers, communication preferences
	- Feedback from management (e.g. performance feedback)
	- Feedback from HR (e.g. hiring/recruitment feedback)
	- Personal development plans
	- Vacation plans
	- Education plans
	- **Availability exceptions**: ask the team about recurring constraints (e.g. school/kindergarten pickup, medical appointments, caregiving) so you can plan meetings and expectations
	- Succession chart
  
- [ ] 3. Design
   
	- Software Architecture and Strategy
	- Data Model (ER)
	- Tech stack summary
	- Third-party products and interfaces, integration points
	- Known technical debt
	- Communications Strategy
	- Languages and Scripts
	- User Interface
	- Design Constraints
	- Performance
	- Access, Roles and Authentication
	- Reporting
	    
- [ ] 4. Development Tools
   
	- Development Environment (who provisions access, standard IDE/config)
	- Version Control System (VCS)
	- Bugtracker
	- Code analysis (static/dynamic tools)
	- Continuous Integration Tool
	- Wiki
	- Automatic documentation building
	   
- [ ] 5. Source Code
   
	- Coding Conventions and Guidelines
	- Solution Structure, main entry points
	- Dependencies
	- Code quality
	- Complexity (e.g. cyclomatic complexity, coupling hotspots)
	- Where deployment/ops scripts live, env/config approach
	- Exception Handling
	- Logging
	- Comments
	- VCS strategy (e.g. gitflow)
	   
- [ ] 6. Build and Release Management
   
	- Build types
	- CI/CD
	- Release and patch strategy
	   
- [ ] 7. QA
   
	- Unit testing and code coverage
	- Integration and API Testing
	- Load Testing
	- Build Verification Testing
	- UI Testing
	- Manual Functional Testing
	- Test data sources, test environment access
	- QA sign-off process
	- Quality gates
	   
- [ ] 8. Deployment
   
	- Environments: DEV, QA, UAT, STAGING, PROD
	- SaaS / Hosted / On-Premise
	- Deployment runbook, who deploys, approval chain
	- Security checking (e.g. vulnerability scanning, compliance checks)
	   
- [ ] 9. Documentation
   
	- Where docs live (Confluence, Notion, SharePoint, repo wiki), doc ownership
	- Location of critical artifacts (runbooks, configs, one place to look first)
	- User Guide
	- Developer Guide
	- Setup Guide
	- Integrations Description (API, RAML, Swagger links)
	   
- [ ] 10. Project management
   
	- Project History (Kickoff meeting presentation, meeting minutes etc)
	- Stakeholders
	- SDLC Description
	- Project Charter
	- Key customers
	- Roadmap
	- Project plan and task tracker (pending work, deadlines, commitments)
	- Risk Management (known risks, open issues, things to watch)
	- Meeting cadence, escalation paths
	- Current budget status
	- Communication Management → see [Communications checklist](COMMUNICATIONS.md)
	- Assumptions and constraints
	- RACI
	- Reporting, Weekly status reports
	- Common/Recurring Tasks
	    
- [ ] 11. System Administration
    
	- Accounts and logins
	- Installed programs/packages
	- Third-party interfaces/equipment
	- Required Licenses & Maintenance agreements
	- Cron jobs
	- Port mapping and firewalls, network diagram
	- Backup/restore, monitoring dashboards
	- System Administrator / DevOps Contacts
	   
- [ ] 12. Maintenance
    
	- SLA
	- Disaster Recovery Plan
	- Change Management
	- Service Desk, incident escalation policies
	- Product Support flow
	- On-call rotation, maintenance windows, known recurring issues
	- Monitoring
	- Logging
- [ ] 13. Contract and Budget

	- Contracts, Invoices, Promises
	- Suppliers and their contacts
	- Vendors and their contacts (including outstaff/contractor agreements, rates, renewal dates)
	- Budget breakdown, approval thresholds
	- Timesheet management policy (in-house vs outstaff/contractor)

- [ ] 14. AI tools and services

	- AI tools used by the team (e.g. Copilot, Cursor, ChatGPT, Claude, internal assistants)
	- AI services and APIs (e.g. OpenAI, Anthropic, Azure AI, internal ML services)
	- Usage policies and guidelines (what may be shared with AI, data handling, acceptable use)
	- Access, licenses, and who provisions (seats, API keys, cost center)
	- Data privacy and compliance (what data can go to which tools; on-prem vs cloud)
	- Ownership and escalation (who decides on new tools, reviews policies, handles incidents)

- [ ] 15. Handover sign-off

	- Handover completed and accepted by [incoming PM]
	- Optional stakeholder sign-off
	- Date and any open follow-ups

## What to read?

- Michael D. Watkins. *The First 90 Days: Proven Strategies for Getting Up to Speed Faster and Smarter, Updated and Expanded*. [Link](https://www.amazon.com/First-90-Days-Strategies-Expanded/dp/1422188612)
- PMBOK / PMI guidance on project closure and handover (for deeper process reference).
- Knowledge handover checklist and project handover best practices (e.g. [Adapt Consulting](https://www.adaptconsultingcompany.com/), [GoSkills](https://www.goskills.com/Project-Management/Resources/Project-handover)).

## Contributing / Feedback

Suggestions and improvements are welcome. See [CONTRIBUTING.md](CONTRIBUTING.md) for how to suggest checklist changes. Open an [issue](https://github.com/wonderu/phf/issues) or submit a pull request.

## License

MIT. See [LICENSE](LICENSE).
