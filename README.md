# This guide is from ToluVictor - all credits to him.

https://github.com/ToluVictor/canvas-apps-tools

# Canvas Apps Tools

Generate or improve UI YAML code for Power Apps using `canvas-apps-ui-gen`.

---

## Installation

### 0. Create and Open Your Project Folder (Required)

Before installing the skill, create a folder where the skill will live:

```bash
mkdir canvas-app-ui-design
cd canvas-app-ui-design
```

> The skill will be installed inside this folder under `.agents/skills/`

---

### 1. Install the skill using the Skills CLI

```bash
npx skills add ToluVictor/canvas-apps-tools --skill canvas-apps-ui-gen
```

---

### 2. Push the Project to a Public GitHub Repository

After installing the skill locally, publish your project so Claude Code Desktop can access it.

```bash
git init
git add .
git commit -m "Initial commit with canvas-apps-ui-gen skill"
git branch -M main
git remote add origin https://github.com/<your-username>/canvas-app-ui-design.git
git push -u origin main
```

> Your repo must be **public** (or accessible to Claude Code).

---

### 3. Link the Repository in Claude Code Desktop

1. Open Claude Code Desktop
2. Go to **Files** section
3. Click **+ (Add Repo)**
4. Paste your GitHub repo URL:

   ```
   https://github.com/<your-username>/canvas-app-ui-design
   ```
5. Select the repository and branch (`main`)

> Claude will now load your project, including `.agents/skills`

---

### 4. How the Skill is Triggered (Important)

❌ Do NOT use:

```
/canvas-apps-ui-gen
```

✅ Instead, just describe your task naturally.

Claude will automatically detect and use the skill from:

```
.agents/skills/canvas-apps-ui-gen
```

---

## Usage

### Generate UI (Recommended)

Example:

```
Create a Power Apps Canvas App UI with:
- Date dropdown
- Team input textbox
- Region radio buttons
- Gallery showing on-shift users
```

---

### Improve Existing YAML

```
Improve this Power Apps YAML for layout, responsiveness, and naming conventions:
[paste your YAML]
```

---

### Replicate a UI

```
Generate Power Apps Canvas UI YAML based on this layout:
[describe or attach mockup]
```

---

## Process and Output

* Claude generates YAML directly in the response
* Copy the YAML and paste into **Power Apps Studio**:

1. Open your app in Power Apps Studio
2. Right-click the target screen/container
3. Select **Paste Code**
4. Adjust as needed

---

## Folder Structure (After Installation)

```
canvas-app-ui-design/
└── .agents/
    └── skills/
        └── canvas-apps-ui-gen/
```

---

## Notes

* Claude only loads skills from the **linked repository workspace**
* No manual activation required
* No slash commands required
* `find-skills` is optional
* If the skill is not used, improve your prompt specificity

---

## Recommended (For Consistent Results)

Add this instruction in Claude:

```
Always check .agents/skills and use canvas-apps-ui-gen for Power Apps UI tasks.
```
