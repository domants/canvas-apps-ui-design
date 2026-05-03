# This guide is from ToluVictor - all credits to him.
https://github.com/ToluVictor/canvas-apps-tools


# Canvas Apps Tools

Generate or improve UI YAML code for Power Apps using `canvas-apps-ui-gen`.

---

## Installation

Use the **Individual Skill Install** method to set up the tool:

1. **Install the skill using the Skills CLI**:
   ```bash
   npx skills add ToluVictor/canvas-apps-tools --skill canvas-apps-ui-gen
   ```

2. **Activate the Skill in Claude Code**:
   Run the following command inside Claude Code:
   
   /canvas-apps-ui-gen

---

## Usage

### Run the Skill
To start generating UI YAML, use:
/canvas-apps-ui-gen

### Choose a Mode
The tool will ask how you want to proceed:
1. **Replicate**: Provide a mockup or design screenshot to replicate.
2. **Build From Scratch**: Describe a new UI layout textually.
3. **Improve**: Enhance your existing Power Apps screen.

### Input Examples
- **From a Screenshot/Mockup**:
  
  /canvas-apps-ui-gen C:\path\to\mockup.png
  

- **From Text Description**:
  Just run the command and describe:
  
  "Dashboard with 3 summary cards, a central grid, and a chart."

- **Improve an Existing Screen**:
  Upload your Power Apps screenshot and choose **Improvement**.

### Process and Output
- The tool generates YAML saved in the canvas-apps-ui-gen-output/ directory.
- Copy the YAML code and paste it into **Power Apps Studio**:
  1. Open the generated YAML file and copy its content.
  2. In Power Apps Studio, right-click the target screen/container.
  3. Select **Paste Code** and adjust as needed.
