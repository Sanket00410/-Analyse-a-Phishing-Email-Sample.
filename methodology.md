# Phishing Email Analysis Methodology

## Overview

This document outlines the systematic methodology employed for analyzing suspicious emails to identify phishing characteristics. The approach combines technical analysis, content examination, and behavioral assessment to provide comprehensive threat evaluation.

## Analysis Framework

### Phase 1: Initial Assessment (5 minutes)
**Objective:** Quick triage to determine if detailed analysis is warranted

**Steps:**
1. **Sender Verification**
   - Check if sender is known/expected
   - Verify sender domain matches organization
   - Look for obvious spoofing indicators

2. **Subject Line Analysis**
   - Identify urgent/threatening language
   - Check for spelling errors
   - Assess legitimacy of claims

3. **Initial Risk Classification**
   - LOW: Likely legitimate, minimal suspicion
   - MEDIUM: Some suspicious elements, requires analysis
   - HIGH: Multiple red flags, likely phishing
   - CRITICAL: Obvious phishing attempt

### Phase 2: Technical Header Analysis (10-15 minutes)
**Objective:** Verify email authenticity through technical examination

**Tools Required:**
- MXToolbox Email Header Analyzer
- Google Admin Toolbox Message Header Analyzer
- Microsoft Message Header Analyzer
- EasyDMARC Header Analyzer

**Analysis Steps:**

1. **Authentication Protocol Verification**
   ```
   Check Results For:
   ✓ SPF (Sender Policy Framework)
   ✓ DKIM (DomainKeys Identified Mail)  
   ✓ DMARC (Domain-based Message Authentication)
   ```

2. **Routing Analysis**
   - Examine Received headers for unusual routing
   - Check originating IP addresses
   - Verify sender server legitimacy
   - Look for suspicious relay patterns

3. **Timestamp Verification**
   - Check for unusual send times
   - Verify timezone consistency
   - Look for rapid-fire sending patterns

**Risk Scoring:**
- Authentication Failure: +3 points each (SPF/DKIM/DMARC)
- Suspicious Routing: +2 points
- Unusual Timestamps: +1 point

### Phase 3: Sender Analysis (5-10 minutes)
**Objective:** Identify domain spoofing and impersonation attempts

**Analysis Components:**

1. **Domain Verification**
   ```bash
   Checks to Perform:
   - Character substitution (0 for O, 1 for l, rn for m)
   - Additional subdomains (security.paypal-update.com)
   - Different TLD (.net instead of .com)
   - Typosquatting (payapl.com, papal.com)
   ```

2. **Display Name vs Email Address**
   - Compare display name with actual email
   - Look for mismatches (CEO display, personal email)
   - Check for unicode/special characters

3. **Organizational Verification**
   - Verify sender exists in organization
   - Check if sender would have authority for request
   - Confirm normal communication patterns

### Phase 4: Content Analysis (10-15 minutes)
**Objective:** Identify social engineering tactics and content anomalies

**Content Categories:**

1. **Language Analysis**
   - Spelling errors and typos
   - Grammar mistakes
   - Unnatural phrasing
   - Inconsistent tone

2. **Social Engineering Tactics**
   ```
   Fear Tactics:
   - Account suspension threats
   - Security breach warnings
   - Legal action threats
   
   Urgency Creation:
   - Time-limited offers
   - Immediate action required
   - Deadline pressures
   
   Authority Exploitation:
   - Executive impersonation
   - Government agency claims
   - IT department requests
   
   Curiosity/Greed:
   - Unexpected winnings
   - Special offers
   - Exclusive opportunities
   ```

3. **Personalization Assessment**
   - Generic vs personalized greetings
   - Use of recipient's actual name
   - Reference to specific accounts/services

### Phase 5: Link and Attachment Analysis (10 minutes)
**Objective:** Identify malicious payloads without system compromise

**Link Analysis Protocol:**
```
NEVER CLICK SUSPICIOUS LINKS
Instead:
1. Hover over links to see destinations
2. Use URL expansion tools for shortened links
3. Check domains against reputation services
4. Verify SSL certificates if necessary
5. Compare with legitimate organization URLs
```

**Attachment Analysis:**
```
Safe Analysis Methods:
1. Check file extensions (especially double extensions)
2. Verify file sizes (unusually large/small)
3. Use online scanning tools
4. Check attachment necessity/expectation
5. Verify sender authority to send attachments

NEVER OPEN SUSPICIOUS ATTACHMENTS
```

### Phase 6: Evidence Documentation (5-10 minutes)
**Objective:** Create comprehensive record for incident response

**Documentation Requirements:**

1. **Technical Evidence**
   - Complete email headers
   - Authentication results
   - Routing information
   - Timestamp data

2. **Content Evidence**
   - Screenshots of email content
   - Link destinations (without clicking)
   - Attachment information
   - Social engineering tactics identified

3. **Analysis Results**
   - Risk score calculation
   - Confidence level assessment
   - Recommended actions
   - Impact assessment

### Risk Scoring Methodology

**Scoring Scale: 1-10 (10 = Highest Risk)**

| Category | Weight | Scoring Criteria |
|----------|--------|------------------|
| Authentication Failure | 25% | SPF/DKIM/DMARC failures |
| Domain Spoofing | 20% | Character substitution, typosquatting |
| Malicious Payload | 25% | Suspicious attachments, malicious links |
| Social Engineering | 15% | Psychological manipulation tactics |
| Content Quality | 10% | Grammar, spelling, professionalism |
| Sender Verification | 5% | Known sender, expected communication |

**Final Risk Calculation:**
```
Overall Risk Score = Σ(Category Score × Weight)
```

**Risk Classifications:**
- **0-3:** LOW - Likely legitimate
- **4-6:** MEDIUM - Suspicious, requires caution  
- **7-8:** HIGH - Likely phishing, avoid interaction
- **9-10:** CRITICAL - Confirmed phishing, immediate action required

### Quality Assurance Checklist

**Pre-Analysis:**
- [ ] Secure analysis environment prepared
- [ ] Analysis tools accessible
- [ ] Documentation template ready
- [ ] Time allocated for thorough analysis

**During Analysis:**
- [ ] All authentication protocols checked
- [ ] Domain spoofing techniques examined
- [ ] Social engineering tactics identified
- [ ] Links analyzed without clicking
- [ ] Attachments characterized safely
- [ ] Evidence properly documented

**Post-Analysis:**
- [ ] Risk score calculated correctly
- [ ] Confidence level assessed
- [ ] Recommended actions specified
- [ ] Report reviewed for accuracy
- [ ] Incident response initiated if required

### Tool Integration Workflow

**Primary Tools:**
1. **MXToolbox** - SPF/DKIM/DMARC verification
2. **Google Admin Toolbox** - Header parsing
3. **Microsoft Header Analyzer** - Authentication analysis
4. **VirusTotal** - URL/attachment reputation
5. **URLVoid** - Domain reputation checking

**Analysis Sequence:**
```
1. Extract headers → MXToolbox analysis
2. Parse routing → Google Admin Toolbox
3. Verify authentication → Microsoft analyzer
4. Check domains → URLVoid/VirusTotal
5. Document findings → CSV/Markdown
```

### Common Pitfalls and Best Practices

**Avoid These Mistakes:**
- ❌ Clicking suspicious links during analysis
- ❌ Opening attachments on production systems
- ❌ Rushing through authentication checks
- ❌ Ignoring subtle domain spoofing
- ❌ Underestimating social engineering

**Best Practices:**
- ✅ Use isolated analysis environment
- ✅ Cross-verify findings with multiple tools
- ✅ Document evidence thoroughly
- ✅ Consider psychological manipulation tactics
- ✅ Maintain chain of custody for evidence
- ✅ Update threat intelligence after analysis

### Continuous Improvement

**Regular Updates Required:**
- Monitor new phishing techniques
- Update tool knowledge and capabilities
- Refine risk scoring based on organizational impact
- Incorporate threat intelligence feeds
- Review and update methodology quarterly

**Training Requirements:**
- Social engineering awareness
- Technical authentication protocols
- Tool proficiency maintenance
- Incident response procedures
- Legal and compliance considerations

This methodology provides a systematic approach to phishing email analysis that balances thoroughness with efficiency while maintaining security throughout the process.