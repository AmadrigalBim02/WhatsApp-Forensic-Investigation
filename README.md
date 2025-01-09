# WhatsApp-Forensic-Investigation

### Overview
This project, explores forensic analysis techniques for WhatsApp Web data. It focuses on examining Random Access Memory (RAM), hard drives, and system snapshots in virtual machine environments. The research uncovers critical insights into user activity, artifact storage, and data recovery mechanisms.

### Key Objectives
- **Analyze RAM**: Recover dynamic session data like chats, poll captions, and user metadata.
- **Examine Hard Drives**: Identify static and persistent artifacts, including real names, emails, deleted messages, and documents.
- **Utilize Snapshots**: Capture transient data such as images, unavailable in RAM or disk analysis, to reconstruct the system's state.

### Tools Used
- **Autopsy 4.21.0**: Forensic analysis of RAM, hard drives, and snapshots.
- **Magnet RAM Capture**: Acquisition of volatile memory data.
- **VMware Workstation Pro**: Controlled virtual machine environment for data isolation.

### Methodology
1. **Environment Setup**:
   - Simulated WhatsApp Web sessions on virtual machines (VM1 & VM2).
   - A dedicated forensic workstation (FW) for artifact analysis.

2. **Data Collection**:
   - Sessions captured under realistic usage scenarios (messages, polls, file sharing, and deletions).
   - Data retrieved via RAM dumps, snapshot files (.vmsn and .vmdk), and disk images.

3. **Analysis Focus**:
   - **RAM**: Extracted transient session data stored in volatile memory.
   - **Snapshots**: Combined memory and disk data to recover ephemeral artifacts.
   - **Hard Drives**: Analyzed JSON and MFT files for persistent data.

### Findings
#### RAM Analysis
- **Artifacts Recovered**: Chat messages, poll captions, user metadata.
- **Limitations**: Media files (e.g., images, audio) were absent, likely encrypted or with minimal memory footprint.

#### Snapshot Analysis
- **Artifacts Recovered**: Images, persistent data (emails, phone numbers).
- **Significance**: Bridged the gap between RAM and hard drive analysis.

#### Hard Drive Analysis
- **Artifacts Recovered**: Persistent user data, deleted messages, documents.
- **Limitations**: Unable to recover transient session-specific artifacts.

### Key Contributions
- Demonstrates the importance of a multi-layered forensic approach.
- Highlights the complementary nature of RAM, snapshot, and hard drive analysis.
- Provides a robust framework for uncovering critical evidence in web-based applications.

### Future Work
- Extend forensic techniques to other platforms (e.g., Facebook, Instagram, Telegram).
- Investigate WhatsApp Desktop and mobile application data storage behaviors.
- Develop advanced integration techniques for automated artifact correlation and improved encryption handling.

### References
For a complete list of references and foundational works, consult the **References** section in the main document.
