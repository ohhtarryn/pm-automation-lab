# Product Note: Dynamic Market Ranking & "Easy Buttons"

## 1. User Intent
Executives need to pivot between different strategic lenses (e.g., "Short-term cash" vs. "Long-term moat") instantly. They want to compare options and for the system to do the heavy lifting of math, but they need the "Final Decision" to feel earned and defensible to their Board.

## 2. Custom Weighting & Resource Constraints
*   **Capacity Mapping:** The system must allow users to input "Team Resources" (Front-end Devs, Back-end Devs, and PMs). These act as a "Friction Multiplier" on Time-to-Market estimates.
*   **The "Market First" Onboarding:** Users cannot access the Comparison Engine until at least two (2) distinct market profiles have been created.
*   **ARR Replacement Logic:** If a user is pivoting from one market to another, the system must calculate "At-Risk ARR." The potential gain in the new market cannot exceed the total TAM of the markets added. There needs to be a way to say if it's a pivot or expansion.
*   **Competition Scaling:** Competition is a "Negative Weight." A 10/10 Competition score should require a 2x increase in "Strategic Value" to maintain the same rank as a 2/10 Competition market.

## 3. Functional Logic: The "Easy Buttons"
The UI should feature a set of preset "Lens Toggles" that apply specific weights to the market data:
*   **"Short-Term Win" (Easy Button):** Heavy weight on current ARR and low "Time to Market."
*   **"Long-Term Dominance" (Easy Button):** Heavy weight on TAM and 5-year CAGR.
*   **The Tie-Breaker (Manual Mode):** If presets results in a "Tie," or if the user wants custom control, provide a "Weighted Settings" drawer. 
    *   Users can manually adjust sliders for TAM, ARR, Growth, and Competition.
    *   The list of markets must reorder in real-time as sliders are moved.

## 4. Experience & Professional Levity
*   **Loading State:** Per the "1-Second Rule," use a skeleton loader. To add "Life" to the corporate tone, include a subtle, high-quality animation of a "Data-Crunching Corgi" or similar professional-yet-fun mascot in the corner of the skeleton frame.
*   **The Dopamine Hit:** When a user clicks "Final Decision," trigger a celebratory UI animation (subtle confetti or a "Decision Confirmed" pulse).

## 5. The Output: Board-Ready Alignment
Clicking "Final Decision" must generate a **"Strategic Alignment Summary."**
*   **Format:** A 3-bullet point script.
*   **Content:** 
    1. Why this market won (based on the active weights).
    2. What we are sacrificing by choosing it (The Opportunity Cost).
    3. A "One-Sentence Pitch" for the Board of Directors.
 
## 6. The "Reality Check" Sidebar (Custom Weights)
To ensure the decision is realistic, provide a sidebar for "Resource Inputs":
*   **Engineering Headcount:** Split inputs for Front-end and Back-end. 
    *   *Logic:* If Back-end count is low, "API-Heavy" markets drop in rank.
*   **PM Bench Strength:** Input for number of PMs.
    *   *Logic:* High PM count allows for "Complex Market Entry"; low PM count favors "Established Market Expansion."
*   **The Onboarding Gate:** If < 2 markets exist, replace the dashboard with an "Empty State" that says: *"A decision requires a choice. Add at least two markets to begin comparing."*

## 7. Success Metrics
*   **Primary:** Number of times a user toggles between different "Easy Buttons" before hitting "Final Decision."
*   **Secondary:** Export rate of the "Strategic Alignment Summary."
