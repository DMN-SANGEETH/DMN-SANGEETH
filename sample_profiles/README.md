# Sample User Profiles

This directory contains 9 realistic sample user profiles for testing and demonstration purposes. Each profile represents a professional in the technology industry with complete data including experience, education, projects, skills, certifications, and more.

## Overview

The sample profiles showcase diverse professionals across different tech domains:

1. **Profile 001** - AI/ML Engineer (Senior, 7 years, India)
2. **Profile 002** - Full-Stack Developer (Mid-level, 4 years, USA)
3. **Profile 003** - DevOps Engineer (Senior, 8 years, UK)
4. **Profile 004** - Data Scientist (Mid-level, 5 years, Japan)
5. **Profile 005** - Mobile Developer (Junior, 2 years, Spain)
6. **Profile 006** - Cybersecurity Engineer (Senior, 9 years, Germany)
7. **Profile 007** - Cloud Architect (Lead, 12 years, Canada)
8. **Profile 008** - Backend Engineer (Mid-level, 6 years, Australia)
9. **Profile 009** - Computer Vision Engineer (Senior, 7 years, Brazil)

## File Structure

```
sample_profiles/
├── profile_001.json    # Individual profile files
├── profile_002.json
├── profile_003.json
├── profile_004.json
├── profile_005.json
├── profile_006.json
├── profile_007.json
├── profile_008.json
├── profile_009.json
├── all_profiles.json   # Combined array of all profiles
└── README.md          # This documentation file
```

## Profile Data Structure

Each profile follows this consistent JSON structure:

```json
{
  "success": true,
  "message": "Profile retrieved",
  "data": {
    "user": { ... },           // User account information
    "profile": { ... },         // Personal and professional details
    "contact": { ... },         // Address and location information
    "experience": {
      "summary": { ... },       // Years of experience breakdown
      "experiences": [ ... ]    // Detailed work history
    },
    "projects": [ ... ],        // Project portfolio with skills
    "education": {
      "tertiary": [ ... ],      // Higher education degrees
      "secondary": [ ... ]      // High school (if applicable)
    },
    "publications": [ ... ],    // Research papers and publications
    "web_links": [ ... ],       // Social and professional links
    "languages": [ ... ],       // Language proficiencies
    "certifications": [ ... ]   // Professional certifications
  }
}
```

## Key Features

### Diversity

- **Industries**: AI/ML, Software Engineering, Data Science, DevOps, Full-Stack Development, Mobile Development, Cybersecurity, Cloud Architecture, Backend Engineering, Computer Vision
- **Experience Levels**: Junior (1-3 years), Mid-level (3-6 years), Senior (6-10 years), Lead (10+ years)
- **Locations**: India, USA, UK, Japan, Spain, Germany, Canada, Australia, Brazil
- **Gender Representation**: Male, Female, Non-binary
- **Age Range**: 24-45 years old

### Realistic Data

- **Complete Work History**: 3-4 experiences per profile with detailed descriptions
- **Project Portfolio**: 3-8 projects per profile with associated skills
- **Education**: University degrees from recognized institutions
- **Certifications**: 3-6 industry certifications from AWS, Google, Microsoft, Coursera, etc.
- **Skills**: 50+ unique skills across all profiles with proficiency ratings
- **Languages**: Multiple language proficiencies reflecting geographic diversity

### Data Quality

- All dates are in ISO format (YYYY-MM-DD or YYYY-MM-DDTHH:MM:SS.mmmmmm)
- Experience dates are chronologically consistent
- Total years of experience match the work history
- Skills are relevant to projects and job roles
- Professional descriptions with bullet points
- Realistic email addresses, phone numbers, and web links

## Usage Examples

### Load a Single Profile

```javascript
// Node.js example
const fs = require('fs');
const profile = JSON.parse(fs.readFileSync('sample_profiles/profile_001.json', 'utf8'));
console.log(profile.data.profile.first_name); // "Aisha"
```

```python
# Python example
import json

with open('sample_profiles/profile_001.json', 'r') as f:
    profile = json.load(f)
    print(profile['data']['profile']['first_name'])  # "Aisha"
```

### Load All Profiles

```javascript
// Node.js example
const fs = require('fs');
const profiles = JSON.parse(fs.readFileSync('sample_profiles/all_profiles.json', 'utf8'));
console.log(`Total profiles: ${profiles.length}`); // 9
```

```python
# Python example
import json

with open('sample_profiles/all_profiles.json', 'r') as f:
    profiles = json.load(f)
    print(f"Total profiles: {len(profiles)}")  # 9
```

### Query Profiles by Industry

```javascript
const profiles = require('./all_profiles.json');
const aiProfiles = profiles.filter(p => 
  p.data.profile.industry.includes('AI')
);
console.log(`AI/ML professionals: ${aiProfiles.length}`);
```

### Extract Skills

```javascript
const profile = require('./profile_001.json');
const allSkills = profile.data.projects.flatMap(project => 
  project.skills.map(s => s.skill)
);
console.log('Skills:', allSkills);
```

## Profile Highlights

### Profile 001 - Aisha Kumar (AI/ML Engineer)
- **Specialty**: Large Language Models, RAG systems
- **Key Skills**: LangChain, GPT-4, PyTorch, HuggingFace
- **Notable**: Published research at NeurIPS and ICML
- **Current**: DeepMind Technologies, Bangalore

### Profile 002 - Marcus Chen (Full-Stack Developer)
- **Specialty**: React, Node.js, TypeScript
- **Key Skills**: React, GraphQL, WebSocket, Redux
- **Notable**: Built real-time payment dashboard
- **Current**: Stripe, San Francisco

### Profile 003 - Sarah Thompson (DevOps Engineer)
- **Specialty**: Kubernetes, CI/CD, Infrastructure as Code
- **Key Skills**: Kubernetes, Terraform, AWS, ArgoCD
- **Notable**: Multi-region K8s platform, 99.99% uptime
- **Current**: Spotify, London

### Profile 004 - Kenji Tanaka (Data Scientist)
- **Specialty**: Machine Learning, Predictive Analytics
- **Key Skills**: Python, TensorFlow, XGBoost, Spark
- **Notable**: Recommendation system for 100M+ users
- **Current**: Rakuten Group, Tokyo

### Profile 005 - Sofia Rodriguez (Mobile Developer)
- **Specialty**: React Native, Cross-platform development
- **Key Skills**: React Native, JavaScript, Redux, Firebase
- **Notable**: Food delivery app with real-time tracking
- **Current**: Glovo, Barcelona

### Profile 006 - Alex Mueller (Cybersecurity Engineer)
- **Specialty**: Penetration Testing, Security Architecture
- **Key Skills**: OSCP, Metasploit, Zero Trust, SIEM
- **Notable**: Red team operations, SOC 2 compliance
- **Current**: Siemens AG, Munich

### Profile 007 - Rajesh Patel (Cloud Architect)
- **Specialty**: AWS, Multi-cloud, Serverless Architecture
- **Key Skills**: AWS, Kubernetes, Terraform, FinOps
- **Notable**: $5M cost reduction through serverless
- **Current**: Shopify, Ottawa

### Profile 008 - Emily Watson (Backend Engineer)
- **Specialty**: Microservices, Event-Driven Architecture
- **Key Skills**: Go, Node.js, Kafka, GraphQL
- **Notable**: Event-driven system processing 1M+ events daily
- **Current**: Atlassian, Sydney

### Profile 009 - Lucas Silva (Computer Vision Engineer)
- **Specialty**: Deep Learning, Object Detection
- **Key Skills**: PyTorch, YOLO, OpenCV, TensorRT
- **Notable**: PhD in Computer Vision, CVPR publications
- **Current**: NVIDIA, São Paulo

## Data Validation

All profiles have been validated for:

- ✅ Valid JSON syntax
- ✅ Complete required fields
- ✅ Chronologically consistent dates
- ✅ Realistic experience duration
- ✅ Appropriate skill levels for experience
- ✅ Industry-relevant technologies
- ✅ Professional language and descriptions
- ✅ Diverse and representative data

## Use Cases

These sample profiles can be used for:

1. **Testing**: Validate profile display, search, and filtering functionality
2. **Demos**: Showcase profile features to stakeholders
3. **Development**: Develop and test UI components without backend dependencies
4. **Training**: Train ML models for profile matching or recommendation systems
5. **Prototyping**: Quickly prototype new features with realistic data
6. **Documentation**: Create user guides and tutorials with example data

## Notes

- All data is fictional and created for demonstration purposes
- Email addresses, phone numbers, and URLs are formatted realistically but are not active
- Certification IDs and credential numbers are randomly generated
- Company names and locations are real but associations are fictional
- Skills and projects reflect current industry trends and technologies

## License

These sample profiles are provided for testing and demonstration purposes. Feel free to use them in your projects.

## Version

- **Version**: 1.0
- **Last Updated**: December 2024
- **Total Profiles**: 9
- **Total Skills**: 220+ unique skills
- **Total Projects**: 54 projects
- **Total Certifications**: 46 certifications
