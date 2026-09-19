# VoIP Support Automation Toolkit

> Identified repeatable patterns and proposed automation opportunities from 500+ L1/L2 tickets. Built platform fluency and contributed to knowledge management.

## 📌 Overview
Built from real L1/L2 support experience at A2N Technologies handling VoIP & SaaS tickets. Analyzed 500+ tickets and found 40% volume is repeatable. Built automation toolkit to reduce manual effort and deflect tickets.

**Live Monitoring:** VoIP Network Health Dashboard for SIP/RTP health, packet loss, call quality.

## 🔍 Problem Identified (From 500+ Tickets)
- **SIP Registration Failures (18%):** 401 Unauthorized, 403 Forbidden, 486 Busy Here
- **One-way Audio (12%):** NAT/Firewall, RTP port block
- **API Integration Failures (10%):** Auth token expiry, rate limiting

**Impact before:** High MTTR, P1 > 4hrs, repetitive L1 manual work

## ✅ Solution Built

### 1. Zendesk Suite Automation
- **Triggers:** Auto-tag `voip_sip_failure`, `one_way_audio`, auto-prioritize P1/P2
- **Automations:** SLA breach alert < 2hr for P1, auto-escalate to L2
- **Macros:** 50+ Canned Responses for SIP 401/403/486, RTP loss, NAT issues
- **Views:** L2 Queue, P1 Open, VoIP Health Issues
- **Help Center:** 30+ KB Articles

### 2. JIRA Service Management
- JQL: `project = SUP AND issuetype = "VoIP Issue" AND status != Done`
- Automation Rules: Auto-link Zendesk ticket to JIRA, SLA tracking
- SLA Management: P1 < 2hr, P2 < 8hr, P3 < 24hr

### 3. Wireshark Filter Library
```bash
# SIP Failures
sip.Status-Code == 401
sip.Status-Code == 403
sip contains "Unauthorized"
sip || rtp
stun

# RTP Analysis
rtp
rtp.ssrc
rtp.marker
rtp.seq
rtp.timestamp

# One-way Audio Debug
sip && ip.addr == <customer_ip>
rtp && udp.port == 10000-20000
