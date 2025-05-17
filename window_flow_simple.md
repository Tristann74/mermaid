```mermaid
flowchart TD
    M[Main Window] --> D[Lead Detail Window]
    D --> Check{Check Contact<br/>Methods}
    
    Check -->|Both Available| Text[Text Message]
    Text --> Email[Email Message]
    Email --> Close1[Close Windows]
    
    Check -->|Text Only| TextOnly[Text Message]
    TextOnly --> Close2[Close Windows]
    
    Check -->|Email Only| EmailOnly[Email Message]
    EmailOnly --> Close3[Close Windows]
    
    Check -->|None Available| Close4[Close Windows]
    
    Close1 --> Next1[Next Lead]
    Close2 --> Next2[Next Lead]
    Close3 --> Next3[Next Lead]
    Close4 --> Next4[Next Lead]

    style M fill:#90EE90
    style D fill:#ADD8E6
    style Text fill:#FFB6C1
    style Email fill:#FFB6C1
    style TextOnly fill:#FFB6C1
    style EmailOnly fill:#FFB6C1
    style Check fill:#FFE4B5
```

# Simple Window Flow

## Basic Process
1. Start at Main Window
2. Open Lead Detail
3. Check Available Contact Methods
4. Take Action Based on Available Methods:
   - Both: Do Text then Email
   - Text Only: Do Text
   - Email Only: Do Email
   - None: Skip Lead
5. Close All Windows
6. Move to Next Lead

## Color Key
- 🟢 Green: Starting Point
- 🔵 Blue: Detail Window
- 🌸 Pink: Action Windows
- 🟡 Yellow: Decision Point 