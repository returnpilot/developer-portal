# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is the ReturnPilot Developer Portal - a documentation site built with Mintlify that provides API documentation for the ReturnPilot returns management platform. The site contains comprehensive API documentation, schemas, enums, and conceptual guides for developers integrating with the ReturnPilot API.

## Development Commands

### Local Development
```bash
# Install Mintlify CLI globally and start development server
npm i -g mint && npm run dev

# Alternative development command
npm run watch
```

### Prerequisites
- Node.js (project uses ES modules)
- Mintlify CLI installed globally

## Project Structure

### Content Organization
- `guide/` - Main documentation content
  - `getting-started/` - Introduction and onboarding
  - `concepts/` - Core API concepts (requests, responses, pagination, rate limiting)
  - `api/` - API endpoint documentation organized by resource
    - `orders/` - Order management endpoints
    - `products/` - Product management endpoints
  - `schemas/` - Data structure definitions
  - `enums/` - Enumeration values and constants
- `snippets/` - Reusable content snippets for API documentation
- `assets/` - Brand assets (logos, banners)

### Configuration Files
- `mint.json` - Mintlify configuration defining navigation, branding, and API settings
- `package.json` - Minimal Node.js configuration for Mintlify

## Documentation Conventions

### File Format
All documentation files use `.mdx` format to support both Markdown and React components.

### Mintlify Components
The documentation uses Mintlify-specific components:
- `<ResponseField>` - For documenting API parameters and response fields
- `<RequestExample>` - For API request examples
- `<ResponseExample>` - For API response examples
- `<Steps>` - For step-by-step instructions
- `<Note>` - For important notes and warnings
- `<Expandable>` - For collapsible content sections

### API Documentation Structure
Each API endpoint follows a consistent structure:
1. Title and overview
2. Endpoint details (URL, method)
3. Request parameters with validation rules
4. Response structure
5. Example requests and responses

## Key Features

### API Configuration
- Base URL: `https://app.returnpilot.co/api/v1`
- Authentication: Bearer token
- API playground is hidden by default

### Navigation Structure
The site is organized into logical sections:
1. Get Started - Introduction and updates
2. Concepts - Core API principles
3. Endpoints - Grouped by resource type
4. Schemas - Data structure definitions
5. Enums - Enumeration constants

## Content Guidelines

### When Adding New Endpoints
1. Create `.mdx` file in appropriate `guide/api/` subdirectory
2. Follow existing documentation structure and component usage
3. Update `mint.json` navigation to include new endpoint
4. Include comprehensive request/response examples
5. Document all validation rules and constraints

### When Adding New Schemas
1. Create `.mdx` file in `guide/schemas/` directory
2. Use `<ResponseField>` components to document all properties
3. Include complete example JSON response
4. Update `mint.json` navigation

### Cross-References
Use relative links to reference other documentation pages (e.g., `/guide/schemas/address` for address schema references).