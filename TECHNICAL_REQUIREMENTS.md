# Technical Requirements for 225 Banksie

## Purpose

This document outlines the critical technical requirements, collaboration guidelines, and context for the **225 Banksie** project. The goal is to avoid misalignment, redundancy, and repeated back-and-forth during the project lifecycle.

---

## General Collaboration Guidelines

1. **Avoid Assumptions**:
    
    - Always confirm the current environment, setup, or context before providing steps or commands.
    - Diagnostics should precede any actionable recommendations.
2. **Ask Questions Proactively**:
    
    - When uncertainty exists about the environment or requirements, prioritize asking clarifying questions over making assumptions.
3. **Explicit Steps**:
    
    - Provide detailed, step-by-step instructions, including commands, expected outputs, and fallback options for potential errors.
4. **Iterative Process**:
    
    - Ensure alignment after every significant step by confirming results before proceeding to the next.

---

## Technical Context

1. **Development Tools**:
    
    - **GitHub**: Repository hosting and version control.
    - **Netlify**: Deployment platform (free tier).
    - **VS Code**: Development environment.
2. **Environment Setup**:
    
    - **Node.js**:
        - Use `nvm` for managing Node.js versions.
        - Always confirm Node.js and npm availability before proceeding with steps.
    - **Python**:
        - Virtual environments (`venv`) are used for Python isolation in other projects.
        - Ensure no conflicts between Node.js and Python environments.
3. **File Management**:
    
    - Required file names for project documentation:
        - `PRD.md`: Product Requirements Document.
        - `TECHNICAL_REQUIREMENTS.md`: This file for collaboration and technical guidelines.
        - Additional files as needed will follow the same `.md` format for consistency.
    - Avoid including sensitive details in `README.md` if the repository becomes public.
4. **Best Practices**:
    
    - Maintain a clear and consistent structure for documentation and project files.
    - Keep `.env` files for environment-specific variables and exclude them from version control.

---

## Diagnostics Workflow

### 1. Check Node.js and npm

Run the following commands to check if Node.js and npm are installed globally:

bash

CopyEdit

`node -v || echo "Node.js is not installed globally. Check with nvm or install globally." npm -v || echo "npm is not installed globally. Check with nvm or install globally."`

### 2. Verify Project Environment

To check if a Python virtual environment is active, run the following command:

bash

CopyEdit

`echo $VIRTUAL_ENV`

To check the Node.js installation path, run the following commands:

bash

CopyEdit

`which node   which npm`

### 3. Search for Project-Specific Installations

Run this command to see if Node.js binaries exist locally in the project:

bash

CopyEdit

`ls -la ./node_modules/.bin/`

### 4. Confirm Package Managers

To verify if `pnpm` or `yarn` is installed, use the following commands:

For `pnpm`:

CopyEdit

`pnpm -v`

For `yarn`:

CopyEdit

`yarn -v`

---

## Critical Requirements

1. **Consistency Across Threads**:
    
    - Always refer back to this file for project context and requirements.
    - Avoid unnecessary repetition by assuming this file is the latest source of truth.
2. **Security Awareness**:
    
    - Avoid exposing sensitive details in public documentation.
    - Ensure Netlify configurations, `.env` files, and deployment settings are secure.
3. **Focus on Context**:
    
    - When transitioning between threads or sessions, review this document for alignment before providing next steps.
4. **Built-in Self-Review**:
    
    - Before providing a response, validate that:
        - The proposed steps align with the project’s current context and technical requirements.
        - Diagnostics are included when assumptions about the environment are required.
        - Clear and actionable fallback options are provided for potential issues.
    - Question the response by asking:
        - "Does this meet the stated objectives and requirements?"
        - "Have I avoided redundancy or incorrect assumptions?"
    - Avoid excessive checks; focus on high-risk areas where misalignment or errors are likely.
5. **File Naming Standards**:
    
    - Use the following file names for documentation:
        - `PRD.md`: For product requirements.
        - `TECHNICAL_REQUIREMENTS.md`: For technical and collaboration guidelines.
        - Any additional documentation should follow the `.md` format and be named descriptively (e.g., `COLLABORATION_GUIDELINES.md`).
    - Consistency in file naming ensures easy reference and alignment across the project.