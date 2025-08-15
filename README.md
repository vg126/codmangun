**Prompt for GitHub Codex/ChatGPT:**```
I need to integrate a large SST (Structural Systematic Transformation) technique database from a JSON file into my DRBanger Legal Research System code.

**TASK:** Replace the fallback SST database in my code with the complete database from `codex_sst.json`

**FILE LOCATION:** `codex_sst.json` (in main repository directory)

**JSON STRUCTURE:** The file contains an array of domain objects, each with techniques:
```json
[
  {
    "domain": "Domain Name",
    "techniques": [
      {
        "name": "Technique Name", 
        "method": "Description of the technique method"
      }
    ]
  }
]
```

**INTEGRATION POINT:** In the JavaScript code, find this line (around line 575):
```javascript
sstDatabase = fallbackSST; // <-- Replace 'fallbackSST' with your JSON array
```

**WHAT TO DO:**
1. Read the contents of `codex_sst.json`
2. Replace the line above with: `sstDatabase = [PASTE_ENTIRE_JSON_CONTENT_HERE];`
3. Ensure proper JavaScript syntax (the JSON should become a valid JavaScript array)
4. Do NOT modify any other part of the code - only replace that single assignment

**EXPECTED RESULT:** All ~250 SST techniques from the JSON file will be integrated and immediately available in:
- Cascading dropdowns (Domain → Technique selection)
- Database browser modal
- Random sampling function  
- Dynamic SST generation system

**IMPORTANT:** Keep the exact JSON structure intact - just convert it from a separate file into an inline JavaScript array assignment.
```

---
l
