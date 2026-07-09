resumeproject

resumeproject is an infrastructure deployment project focused on automating the setup of basic Windows Server environments for small organizations.

The long-term goal is to help IT administrators, small businesses, schools, nonprofits, MSPs, and homelab users deploy repeatable Windows infrastructure using a guided workflow and declarative configuration files.

Project Goal

The goal of this project is to build a tool that can help provision core Windows infrastructure such as:

Active Directory
DNS
DHCP
Organizational Units
Users and groups
File shares
Baseline Group Policy
Physical workstation domain-join support

This project is currently in the early planning and proof-of-concept stage.

Current Focus

The first development milestone is:

resumeproject 0.1 — Foundation & Remote Connection POC

The purpose of this milestone is to prove that the project can connect to a Windows Server target and run basic remote PowerShell commands.

Example future command:

resumeproject test-connection --target 192.168.50.10

Expected future output:

Connecting to 192.168.50.10...

Connected successfully.

Hostname: DC01
User: Administrator

Target is ready for deployment.
Planned MVP

The MVP will focus on initial infrastructure deployment, not long-term endpoint management.

Planned MVP features include:

Desktop application
Declarative YAML configuration
Deployment plan preview
Windows Server target configuration
Active Directory deployment
DNS configuration
DHCP configuration
User and group generation
File share creation
Basic Group Policy configuration
Deployment reporting
Rollback and error handling
Example Use Case

A small business has a Windows Server machine and several physical Windows workstations.

An IT administrator uses resumeproject to configure the server with Active Directory, DNS, DHCP, users, groups, file shares, and baseline policies.

Employee workstations remain physical devices and are joined to the domain after the server infrastructure is deployed.

Project Status

This project is currently under active planning and early development.

Current priorities:

Define the project architecture.
Create architecture decision records.
Build the initial repository structure.
Create example YAML configurations.
Build a basic CLI skeleton.
Prove remote PowerShell execution against a Windows Server target.
Repository Structure

Planned structure:

resumeproject/
├── README.md
├── LICENSE
├── docs/
│   ├── MVP.md
│   ├── ARCHITECTURE.md
│   └── decisions/
├── examples/
│   └── small-business.yml
├── src/
├── tests/
└── scripts/
Architecture Principles

This project follows these core design principles:

Backend/core first, GUI second
YAML as the source of truth
Modular provider-based design
Deployment workflow: validate, plan, preview, approve, execute, verify, report
Rollback-aware failure handling
Physical Windows workstations are supported through domain-join workflows
Hyper-V may be supported for testing or virtualized server deployments, but the project should not be tightly coupled to Hyper-V
License

This project is licensed under the MIT License. See the LICENSE file for details.

