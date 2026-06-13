# False Positive Validation Workflow

Workflow ID: FP-001

## Objective

Provide a repeatable process for validating reported security findings and determining whether remediation is required.

## Input Sources

- SAST
- SCA
- DAST
- Infrastructure Scanners
- Penetration Testing
- Responsible Disclosure

## Validation Process

### Step 1: Collect Evidence

- Tool output
- File location
- Dependency information
- Affected component

### Step 2: Technical Verification

- Review source code
- Verify dependency versions
- Review deployment architecture
- Confirm exploit prerequisites

### Step 3: Reachability Analysis

- Is vulnerable code reachable?
- Is the affected component enabled?
- Are attack preconditions satisfied?

### Step 4: Classification

#### Genuine

Criteria:

- Technically reproducible
- Reachable attack path exists
- Security impact confirmed

#### False Positive

Criteria:

- Non-reachable code
- Mitigating controls exist
- Incorrect tool detection
- Dependency resolution removes exposure

### Step 5: Documentation

Record:

- Evidence
- Justification
- Classification
- Approval

## Outputs

- Genuine Finding
- False Positive Finding
- Risk Acceptance Candidate

