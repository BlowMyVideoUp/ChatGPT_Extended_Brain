
    # README - Daily Scan Logic Protocol

    **Last Updated:** 2025-04-20

    ## 🔁 1. SCAN STRATEGY
    - Every file uploaded must trigger 108 separate scans (one for each known subdirectory).
- Do NOT rely only on keyword matching. Keywords are only 10% of the logic.
- Instead, use natural language cues and behavioral context to extract logic, problems, and fixes.

    ## 🔍 2. DETECTION RULES
    - Look for **frustration markers** to identify problems:
  - “this broke”, “didn’t work”, “blank zip”, “manifest missing”
- Look for **uploaded code** immediately after a problem → that’s BROKEN CODE
- Track AI responses with:
  - Fix attempts (uploaded/generated)
  - Confirmation or rejection

    ## ✅ 3. CLASSIFICATION
    For every scanned finding, classify it:

- ✅ Successful Solution
  - Triggered by: “great”, “fantastic”, “it worked”, “you’re a superhero”, “you’re Babe Ruth”
- ❌ Failed Solution
  - Triggered by: “nope, still broken”, “that didn’t work”, “no change”, “worse than before”
- BROKEN CODE
  - Any raw code uploaded after frustration, failure, or error message
