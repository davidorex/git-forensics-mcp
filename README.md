# Git Forensics MCP

A specialized Model Context Protocol (MCP) server for deep git repository investigation and analysis. This forensics tool provides detailed insights into repository history, branch relationships, and development patterns, focusing solely on git repository analysis rather than general GitHub or git operations.

<a href="https://glama.ai/mcp/servers/xp4kpz0mdl"><img width="380" height="200" src="https://glama.ai/mcp/servers/xp4kpz0mdl/badge" alt="Git Forensics MCP server" /></a>

## Features

The server provides four main analysis tools:

1. **Branch Overview** (`get_branch_overview`)
   - Provides high-level overview of branch states and relationships
   - Analyzes last commits, commit counts, and merge bases
   - Generates statistical summaries of branch activities

2. **Time Period Analysis** (`analyze_time_period`)
   - Analyzes detailed development activity in specific time periods
   - Categorizes commits (feature, fix, refactor, docs, other)
   - Provides activity summaries with commit patterns

3. **File Changes Analysis** (`analyze_file_changes`)
   - Tracks changes to specific files across branches
   - Identifies potential conflict areas
   - Provides risk assessment for file modifications
   - Generates recommended review order based on risk levels

4. **Merge Recommendations** (`get_merge_recommendations`)
   - Determines optimal merge strategies
   - Assesses conflict risks
   - Identifies code hotspots
   - Provides step-by-step merge guidance

## Input Parameters

Each tool requires specific parameters:

- `repoPath`: Path to the git repository
- `branches`: Array of branch names to analyze
- `outputPath`: Path where analysis results will be written
- Additional tool-specific parameters:
  - `timeRange`: Start and end dates for period analysis
  - `files`: Array of file paths for file change analysis

## Output Format

All tools output JSON files containing:
- Detailed analysis results
- Summary statistics
- Risk assessments (where applicable)
- Recommendations based on analysis

## Technical Details

- Built with TypeScript
- Uses MCP SDK for server implementation
- Executes git commands through child processes
- Provides error handling and validation
- Runs on stdio transport

## Dependencies

- @modelcontextprotocol/sdk
- Node.js
- Git (must be installed and accessible)

## Usage

The server runs as an MCP service and can be integrated with any MCP-compatible client. All analysis results are written to specified output files in JSON format.

## Contributing and License

This project is licensed under the Apache License, Version 2.0 - see the [LICENSE.txt](LICENSE.txt) file for details.

### Collaboration Welcome
Forks and contributions welcome. 

All contributions will be under the Apache License 2.0. This permissive license allows you to:
- Use the code commercially
- Modify and distribute the code
- Create derivative works
- Include in other projects

Copyright 2025. Licensed under the Apache License, Version 2.0; you may not use this project except in compliance with the License. You may obtain a copy of the License at http://www.apache.org/licenses/LICENSE-2.0
