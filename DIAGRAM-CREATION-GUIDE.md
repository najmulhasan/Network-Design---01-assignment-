# Visual Network Diagram Creation Guide

## Quick Start (5-10 Minutes)

Follow these steps to create your professional network architecture diagram in draw.io:

---

## Step 1: Setup Draw.io (1 minute)

1. Go to https://app.diagrams.net/
2. Click **"Create New Diagram"**
3. Choose **"Blank Diagram"**
4. Name it: `Real-Estate-Network-Architecture`

---

## Step 2: Add AWS Icons Library (1 minute)

1. Click **"More Shapes"** (+ icon on the left panel)
2. In the search box, type: **"AWS"**
3. Check these boxes:
   - ✅ **AWS 19** (latest AWS icons)
   - ✅ **AWS 17** (backup icons)
4. Click **"Apply"**
5. The AWS shapes will now appear in your left sidebar

---

## Step 3: Create the Layout Structure (2 minutes)

### A. Add Global Layer (Top)
1. Drag a **large rectangle** from General shapes
2. Label it: **"Global Layer - Route 53 & CloudFront"**
3. Color: Light blue (#E3F2FD)
4. Add inside it:
   - AWS Icon: **Route 53** (from AWS19 > Networking & Content Delivery)
   - AWS Icon: **CloudFront** (from AWS19 > Networking & Content Delivery)
   - AWS Icon: **AWS Shield** (from AWS19 > Security, Identity, & Compliance)

### B. Add Two Regions (Side by Side)
1. Drag two large rectangles below the global layer
2. **Left Rectangle**: Label "**Region 1 - US-EAST-1**" (Color: Light Green #E8F5E9)
3. **Right Rectangle**: Label "**Region 2 - EU-WEST-1**" (Color: Light Orange #FFF3E0)

### C. Add Availability Zones (2 per region)
Inside each region rectangle:
1. Add two medium rectangles
2. Label them: **"AZ-1a"** and **"AZ-1b"** (in Region 1)
3. Label them: **"AZ-2a"** and **"AZ-2b"** (in Region 2)
4. Color: White with border

---

## Step 4: Build VPC Structure in Each AZ (3 minutes)

### For Each Availability Zone, add these layers from top to bottom:

#### Layer 1: PUBLIC SUBNET (Light Yellow #FFFDE7)
Add a rectangle labeled "Public Subnet - 10.0.1.0/24"

**Drag these AWS icons inside:**
- **Internet Gateway** (AWS19 > Networking & Content Delivery)
- **NAT Gateway** (AWS19 > Networking & Content Delivery)
- **Application Load Balancer** (AWS19 > Networking & Content Delivery > Elastic Load Balancing)
- **EC2** icon with label "Bastion Host" (AWS19 > Compute)

#### Layer 2: PRIVATE SUBNET - APPLICATION TIER (Light Purple #F3E5F5)
Add a rectangle labeled "Private Subnet - App - 10.0.10.0/24"

**Drag these AWS icons inside:**
- **Auto Scaling** group (AWS19 > Compute > Auto Scaling)
- **EC2** instances (3-4 icons) (AWS19 > Compute)
- **ECS/EKS** icon (AWS19 > Containers)
- **API Gateway** (AWS19 > Networking & Content Delivery)

Add text labels:
- "Search API"
- "Bidding Service"
- "Chat Service (WebSocket)"

#### Layer 3: PRIVATE SUBNET - DATA TIER (Light Red #FFEBEE)
Add a rectangle labeled "Private Subnet - Data - 10.0.20.0/24"

**Drag these AWS icons inside:**
- **RDS** (AWS19 > Database) - Label: "PostgreSQL Multi-AZ"
- **ElastiCache** (AWS19 > Database) - Label: "Redis"
- **OpenSearch** (AWS19 > Analytics) - Label: "Property Search"

#### Layer 4: PRIVATE SUBNET - INTEGRATION TIER (Light Cyan #E0F7FA)
Add a rectangle labeled "Private Subnet - Integration - 10.0.30.0/24"

**Drag these AWS icons inside:**
- **Lambda** (AWS19 > Compute) - Label: "3rd Party API Integration"
- **SQS** (AWS19 > Application Integration)
- **SNS** (AWS19 > Application Integration)
- **EventBridge** (AWS19 > Application Integration)

#### Layer 5: PRIVATE SUBNET - DEVELOPER (Light Gray #F5F5F5)
Add a rectangle labeled "Private Subnet - Dev - 10.0.40.0/24"

**Drag these AWS icons inside:**
- **VPN Gateway** (AWS19 > Networking & Content Delivery)
- **EC2** with label "Dev Instances"
- **CodePipeline** (AWS19 > Developer Tools)

---

## Step 5: Add Cross-Region Components (1 minute)

On the right side or bottom, create a section labeled "Cross-Region Components":

**Add these AWS icons:**
- **S3** (AWS19 > Storage) - Label: "Cross-Region Replication"
- **Transit Gateway** (AWS19 > Networking & Content Delivery)
- **Global Accelerator** (AWS19 > Networking & Content Delivery)
- **VPC Peering** connection icon

---

## Step 6: Add Security Layer (1 minute)

Create a sidebar or box labeled "Security & Monitoring":

**Add these AWS icons:**
- **AWS WAF** (AWS19 > Security, Identity, & Compliance)
- **Security Groups** icon
- **CloudWatch** (AWS19 > Management & Governance)
- **CloudTrail** (AWS19 > Management & Governance)
- **Secrets Manager** (AWS19 > Security, Identity, & Compliance)
- **KMS** (AWS19 > Security, Identity, & Compliance)

---

## Step 7: Connect Components with Arrows (2 minutes)

### Add connections showing traffic flow:

1. **From Route 53** → **to both regions** (thick arrow)
2. **From Internet Gateway** → **to ALB** (arrow)
3. **From ALB** → **to EC2 instances** (arrow)
4. **From EC2** → **to RDS/Redis/OpenSearch** (arrows)
5. **From Lambda** → **External** (dotted arrow labeled "3rd Party APIs")
6. **Between regions** → **Transit Gateway connections** (bidirectional arrow)
7. **From VPN** → **to Dev Subnet** (encrypted arrow)

### Arrow Tips:
- Use **solid arrows** for internal traffic
- Use **dotted arrows** for external/internet traffic
- Use **thick arrows** for high-volume traffic
- Use **bidirectional arrows** for two-way communication

---

## Step 8: Format and Polish (1 minute)

### Add Visual Polish:
1. **Group similar items**: Select multiple items and right-click → Group
2. **Align components**: Use the Arrange menu → Align
3. **Add a legend** (small box in corner):
   - Traffic Flow: →
   - External API: ···>
   - Cross-Region: ⟷
4. **Add title**: Large text box at top: "Real Estate Finder Platform - Multi-Region Network Architecture"
5. **Add your name and date** at bottom

### Color Consistency:
- Public Subnets: Yellow
- Application Tier: Purple
- Data Tier: Red
- Integration Tier: Cyan
- Developer: Gray
- Region 1: Green border
- Region 2: Orange border

---

## Step 9: Export the Diagram (30 seconds)

1. Click **File** → **Export as** → **PNG**
2. Settings:
   - ✅ Check "Transparent Background" (optional)
   - ✅ Check "Selection Only" (uncheck to export all)
   - Border Width: 10
   - Zoom: 100%
3. Click **Export**
4. Save as: `network-architecture-diagram.png`
5. Save the file to: `c:\Users\user\Desktop\networking assignment\`

**Also export as SVG** (for high quality):
1. Click **File** → **Export as** → **SVG**
2. Save as: `network-architecture-diagram.svg`

---

## Step 10: Add to README (30 seconds)

1. In your README.md, find the line:
   ```
   **Diagram File**: `network-architecture-diagram.png` (To be added)
   ```

2. Replace it with:
   ```
   **Diagram File**: `network-architecture-diagram.png`
   
   ![Network Architecture Diagram](network-architecture-diagram.png)
   ```

---

## Quick Reference: AWS Icons You Need

| Component | Location in AWS19 Library | Notes |
|-----------|---------------------------|-------|
| Route 53 | Networking & Content Delivery | DNS |
| CloudFront | Networking & Content Delivery | CDN |
| VPC | Networking & Content Delivery | Network container |
| Internet Gateway | Networking & Content Delivery | Public access |
| NAT Gateway | Networking & Content Delivery | Outbound only |
| ALB | Networking & Content Delivery > ELB | Load balancer |
| EC2 | Compute | Virtual servers |
| Auto Scaling | Compute | Scaling group |
| ECS/EKS | Containers | Container service |
| RDS | Database | Relational DB |
| ElastiCache | Database | Redis/Memcached |
| OpenSearch | Analytics | Search engine |
| Lambda | Compute | Serverless functions |
| S3 | Storage | Object storage |
| SQS | Application Integration | Message queue |
| SNS | Application Integration | Notifications |
| VPN Gateway | Networking & Content Delivery | VPN access |
| Transit Gateway | Networking & Content Delivery | Network hub |
| WAF | Security, Identity, & Compliance | Firewall |
| CloudWatch | Management & Governance | Monitoring |
| Secrets Manager | Security, Identity, & Compliance | Secret storage |

---

## Alternative: Use Draw.io Template Code

If you want to speed up the process, I can provide you with XML code that you can import into draw.io. Let me know if you'd like that option!

---

## Tips for a Professional Diagram

✅ **DO:**
- Use consistent colors for each tier
- Keep spacing uniform
- Align components neatly
- Use clear, readable fonts (12-14pt)
- Add a legend/key
- Show traffic flow with arrows
- Label all major components

❌ **DON'T:**
- Overcrowd the diagram
- Use too many colors
- Forget to label components
- Make text too small
- Cross too many arrows

---

## Expected Result

Your final diagram should show:
- ✅ 2 Regions clearly separated
- ✅ 2 Availability Zones per region
- ✅ 5 subnet tiers per AZ
- ✅ All major AWS services with icons
- ✅ Traffic flow arrows
- ✅ Security and monitoring components
- ✅ Cross-region connections
- ✅ Professional appearance

---

## Time Estimate
- **First time**: 10-15 minutes
- **If you follow this guide exactly**: 5-8 minutes

---

## Need Help?
If you get stuck, the ASCII diagram in your README.md shows exactly what should be connected to what. Use it as your blueprint!

---

**Good luck! Your diagram will look professional and comprehensive when complete.**
