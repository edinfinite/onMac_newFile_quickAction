# onMac_newFile_quickAction

# CreateNewFile_with_shortcut_keys

Automator extension to create a new file with right-click (Mac).

## Instructions

### Step 1: Create the Automator Quick Action

1. **Open Automator**:
   - Press `Command + Space` to open Spotlight.
   - Type `Automator` and press `Enter`.

2. **Create a New Quick Action**:
   - Select `Quick Action` in the dialog that appears.
   - Click `Choose`.

3. **Configure the Quick Action**:
   - Set `Workflow receives current` to `files or folders` in `Finder.app`.

4. **Add Run AppleScript Action**:
   - In the Library on the left, search for `Run AppleScript`.
   - Drag `Run AppleScript` to the workflow area on the right.

5. **Enter the AppleScript Code**:
   - Clear the default code and paste the following script:
     ```applescript
     on run {input, parameters}
         tell application "Finder" to make new file at (the target of the front window) as alias
         return input
     end run
     ```

6. **Save the Quick Action**:
   - Save the Quick Action by selecting `File > Save` or pressing `Command + S`.
   - Name it something descriptive, like `Create New File`.
   - Click `Save`.

### Step 2: Assign a Shortcut Key

1. **Open System Preferences**:
   - Go to `Keyboard`.
   - Select the `Shortcuts` tab.

2. **Add the Shortcut**:
   - Select `Services` from the left sidebar.
   - Find your Quick Action under `General` or the appropriate section.
   - Click on `add shortcut` next to it and assign your desired key combination.

For example, you can use `Ctrl + Option + Command + L` as your shortcut. *Remeber need to be in a folder for this to work*

### Usage

1. **Open Finder**:
   - Navigate to the folder where you want to create a new file.

2. **Use the Shortcut Key**:
   - Press the shortcut key combination you set (e.g., `Ctrl + Option + Command + N`).

This will create a new file named `untitled` in the folder you are currently in.

### Note
- right click from trackpad and mouse...nextup
