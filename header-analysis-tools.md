# Email Header Analysis Tools Reference

## Free Online Header Analysis Tools

### 1. MXToolbox Email Header Analyzer
**URL:** https://mxtoolbox.com/EmailHeaders.aspx
**Best For:** Comprehensive SPF, DKIM, DMARC verification

**Features:**
- Complete header parsing and analysis
- Authentication protocol verification
- Routing path visualization
- Spam score assessment
- IP reputation checking

**How to Use:**
1. Copy complete email headers (View > Message Source)
2. Paste headers into MXToolbox analyzer
3. Review authentication results
4. Check routing information for anomalies
5. Document SPF/DKIM/DMARC failures

**Key Output Indicators:**
-  SPF: PASS/FAIL status
-  DKIM: Signature verification results
-  DMARC: Policy compliance check
-  Routing anomalies flagged

### 2. Google Admin Toolbox Message Header Analyzer
**URL:** https://toolbox.googleapps.com/apps/messageheader/
**Best For:** Detailed header parsing and Gmail-specific analysis

**Features:**
- Clean, user-friendly interface
- Detailed hop-by-hop routing analysis
- Time zone and delay analysis
- Google Workspace integration
- Authentication result interpretation

**Analysis Process:**
1. Access Google Admin Toolbox
2. Paste raw email headers
3. Click "Analyze" for detailed breakdown
4. Review routing path and timestamps
5. Check authentication status

**Specialized Capabilities:**
- Gmail-specific header interpretation
- Detailed routing visualization
- Time delay analysis between hops
- Clean formatting for documentation

### 3. Microsoft Message Header Analyzer
**URL:** https://mha.azurewebsites.net/
**Best For:** Microsoft ecosystem email analysis

**Features:**
- Microsoft-focused authentication analysis
- Visual interface with clear results
- Office 365 specific insights
- Easy-to-read output format
- Anti-spam scoring information

**Usage Instructions:**
1. Navigate to Microsoft Header Analyzer
2. Input complete email headers
3. Review parsed authentication results
4. Check for Microsoft-specific indicators
5. Export results for documentation

**Strengths:**
- Excellent for Office 365/Exchange environments
- Clear visual presentation of results
- Detailed authentication explanations
- Anti-spam scoring integration

### 4. EasyDMARC Email Header Analyzer
**URL:** https://easydmarc.com/tools/email-header-analyzer
**Best For:** DMARC policy analysis and DNS record verification

**Key Features:**
- Comprehensive DMARC analysis
- DNS record verification
- SPF record parsing
- DKIM signature analysis
- Deliverability insights

**Analysis Workflow:**
1. Submit email headers to tool
2. Review comprehensive authentication report
3. Check DNS record alignment
4. Verify DMARC policy compliance
5. Document policy failures

**Unique Capabilities:**
- Deep DMARC policy analysis
- DNS record health checking
- Deliverability scoring
- Policy recommendation engine

### 5. Zoho Email Header Analyzer
**URL:** https://zoho.com/toolkit/email-header-analyzer.html
**Best For:** Multi-tool analysis platform

**Features:**
- Comprehensive toolkit integration
- Header hop analysis
- Authentication verification
- Routing path examination
- IP geolocation data

### 6. WhatIsMyIP Email Header Analyzer
**URL:** https://whatismyip.com/email-header-analyzer/
**Best For:** IP analysis and geolocation

**Specialized Features:**
- Detailed IP geolocation
- Sender verification tools
- Routing path analysis
- Reverse DNS lookups
- ASN information

## Tool Selection Guide

### For Beginners:
**Recommended:** Google Admin Toolbox
- Clean interface
- Easy interpretation
- Good documentation

### For Technical Analysis:
**Recommended:** MXToolbox
- Comprehensive feature set
- Detailed technical information
- Professional reporting

### For Microsoft Environments:
**Recommended:** Microsoft Header Analyzer
- Office 365 optimized
- Exchange-specific insights
- Clear authentication results

### For DMARC Focus:
**Recommended:** EasyDMARC
- Deep DMARC analysis
- Policy compliance checking
- DNS record verification

## Analysis Best Practices

### Header Extraction Methods:

**Gmail:**
1. Open email
2. Click "Show original" (three dots menu)
3. Copy entire content from text box

**Outlook:**
1. Open email
2. File > Properties > Internet Headers
3. Copy header content

**Thunderbird:**
1. View > Headers > All
2. Right-click > View Source
3. Copy header section

**Apple Mail:**
1. View > Message > All Headers
2. Select and copy header content

### Common Analysis Patterns:

**Authentication Failures:**
```
SPF: FAIL - Most critical indicator
DKIM: FAIL - Signature issues
DMARC: FAIL - Policy violations
```

**Suspicious Routing:**
```
Private IP addresses in public routing
Unknown or suspicious mail servers
Geographically inconsistent routing
Missing reverse DNS entries
```

**Timing Anomalies:**
```
Unusual send times (middle of night)
Rapid-fire sending patterns
Timezone inconsistencies
Future/past timestamp errors
```

## Tool Comparison Matrix

| Tool | SPF | DKIM | DMARC | UI Quality | Speed | Export |
|------|-----|------|-------|-----------|-------|--------|
| MXToolbox | ✅ | ✅ | ✅ | Good | Fast | Yes |
| Google | ✅ | ✅ | ✅ | Excellent | Fast | No |
| Microsoft | ✅ | ✅ | ✅ | Good | Medium | Limited |
| EasyDMARC | ✅ | ✅ | ✅ | Good | Medium | Yes |
| Zoho | ✅ | ✅ | ✅ | Fair | Fast | Yes |
| WhatIsMyIP | ✅ | ✅ | ✅ | Fair | Fast | Limited |

## Advanced Analysis Techniques

### Cross-Validation Approach:
1. Use primary tool (MXToolbox) for initial analysis
2. Verify results with secondary tool (Google)
3. Check specific features with specialized tools
4. Document discrepancies for investigation
5. Use manual analysis for complex cases

### Automation Possibilities:
- API integration where available
- Batch processing for multiple emails
- Automated report generation
- Integration with SIEM platforms
- Threat intelligence enrichment

## Troubleshooting Common Issues

### Tool Access Problems:
- Try different browsers if loading fails
- Check for ad-blocker interference
- Use alternative tools if primary unavailable
- Clear browser cache for persistent issues

### Header Parsing Errors:
- Ensure complete header is copied
- Check for special characters or encoding
- Try different extraction methods
- Manual parsing if automated tools fail

### Result Interpretation:
- Cross-reference multiple tools
- Understand tool-specific terminology
- Consider environmental factors
- Consult documentation for edge cases

## Documentation Templates

### Analysis Report Template:
```
Tool Used: [Tool Name]
Analysis Date: [Date/Time]
Authentication Results:
- SPF: [PASS/FAIL] - [Details]
- DKIM: [PASS/FAIL] - [Details]  
- DMARC: [PASS/FAIL] - [Details]
Routing Analysis: [Summary]
Risk Assessment: [LOW/MEDIUM/HIGH/CRITICAL]
Confidence Level: [Percentage]
Recommendations: [Actions Required]
```

### Evidence Collection:
- Screenshot tool results
- Save raw analysis output
- Document tool versions used
- Record analysis timestamp
- Preserve original headers

This comprehensive tool reference enables systematic and thorough email header analysis using free, accessible online resources while maintaining professional analysis standards.
