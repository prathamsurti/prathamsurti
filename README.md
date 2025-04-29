- 👋 Hi, I’m @prathamsurti

<!---
prathamsurti/prathamsurti is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
graph TD
    A[Start: Designer works in Figma] --> B{Needs Design Feedback?};
    B -- Yes --> C[Opens Heurica/Lovable.dev Plugin];
    C --> D(Verify Logged In);
    D --> E[Selects Figma Frame(s)];
    E --> F[Clicks 'Run Audit'];
    F --> G((System: Plugin sends data to Backend));
    G --> H((System: Backend analyzes Heuristics & Copy));
    H --> I((System: Backend sends results to Plugin));
    I --> J[Plugin displays Score, Issues, Suggestions];
    J --> K[Designer reviews feedback within Figma];
    K --> L{Make Design Changes?};
    L -- Yes --> M[Designer adjusts Figma design];
    M --> E; %% Option to re-run audit
    L -- No --> N{Export Report?};
    N -- Yes --> O[Clicks 'Export Report'];
    O --> P((System: Backend generates PDF/Notion Report));
    P --> Q[Designer downloads/views Report];
    Q --> R[Designer shares Report];
    R --> T[End: Feedback received & Report obtained];
    N -- No --> S[Designer continues work];
    B -- No --> S;
    S --> A; %% Loop back or end work session

%% Styling nodes for clarity (optional)
classDef systemProcess fill:#f9f,stroke:#333,stroke-width:2px;
class G,H,I,P systemProcess;
