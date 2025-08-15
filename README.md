Prompt for ChatGPT Codex:

```
Convert the following SST techniques text into a JSON structure. For each domain section, extract all the numbered techniques and format them according to this template:

TEMPLATE STRUCTURE:
```json
[
  {
    "domain": "Domain Name",
    "techniques": [
      {
        "name": "Technique Name",
        "method": "Brief description of the transformation method or application"
      }
    ]
  }
]
```

EXTRACTION RULES:
1. Create one domain object for each major section (e.g., "Functional Programming", "Geo and Spatial", "Legal", "Mathematical", "Military")
2. For each numbered technique, extract:
   - name: The technique title (remove emoji and number)
   - method: The main explanation/description (1-2 sentences, combine if needed)
3. Remove citations, footnotes, and example details - keep only the core method description
4. If a technique has multiple paragraphs, combine the key concepts into a concise method description
5. For simulated techniques, include "Simulated" in the name
6. Skip any introductory text, conclusions, or reference sections

INPUT TEXT:
[Paste your SST techniques document here]

OUTPUT: Valid JSON array following the template structure above.
```

## Example of Expected Output Format:

```json
[
  {
    "domain": "Functional Programming",
    "techniques": [
      {
        "name": "Beta-reduction",
        "method": "Beta-reduction applies a function to its argument by substituting the argument into the function's body, simplifying expressions through lambda calculus operations."
      },
      {
        "name": "Eta-conversion", 
        "method": "Eta-conversion simplifies a function by removing unnecessary lambda abstractions when the function applies another function to its argument unchanged."
      }
    ]
  },
  {
    "domain": "Geo and Spatial",
    "techniques": [
      {
        "name": "Map Projection Transformation",
        "method": "Map projection converts spherical Earth coordinates into flat, two-dimensional representations using mathematical formulas that preserve specific properties like area, distance, or angles."
      }
    ]
  }
]
```