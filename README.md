# VSCodeVim Settings

VSCodeVim is a Vim emulator for Visual Studio Code + Commands

## Table of Content

-   [Vim Shortcuts](#-vim-shortcuts)
-   [VSCode Shortcuts](#-vscode-shortcuts)
-   [View Commands](#-view-commands)
-   [Emmet Commands](#-emmet-commands)
-   [Git Commands](#-git-commands)
-   [Debug Commands](#-debug-commands)

<br>

## Vim Shortcuts

### Normal Mode

| Status             | Command      | Description                   |
| ------------------ | ------------ | ----------------------------- |
| :white_check_mark: | `<leader>` l | Last Character In The Line    |
| :white_check_mark: | `<leader>` h | First Character In The Line   |
| :white_check_mark: | K            | Move 5 Line Up                |
| :white_check_mark: | J            | Move 5 Line Down              |
| :white_check_mark: | CTRL n       | Turn Off Search Highlighting  |
| :white_check_mark: | CTRL j       | View Focus Above Editor Group |
| :white_check_mark: | CTRL k       | View Focus Below Editor Group |
| :white_check_mark: | CTRL h       | View Focus Left Editor Group  |
| :white_check_mark: | CTRL l       | View Focus Right Editor Group |

<br>
<details>
 <summary><strong>Settings Example</strong> (click to expand)</summary>

Below is an example of a [settings.json](https://code.visualstudio.com/Docs/customization/userandworkspace) file with settings relevant to VSCodeVim:

```json
{
	"vim.normalModeKeyBindingsNonRecursive": [
		{
			"before": ["J"],
			"after": ["5", "j"]
		},
		{
			"before": ["K"],
			"after": ["5", "k"]
		},
		{
			"before": ["<Leader>", "l"],
			"after": ["$"]
		},
		{
			"before": ["<Leader>", "h"],
			"after": ["^"]
		},
		{
			"before": ["<C-n>"],
			"commands": [":nohl"]
		},
		{
			"before": ["<C-h>"],
			"after": ["<C-w>", "h"]
		},
		{
			"before": ["<C-j>"],
			"after": ["<C-w>", "j"]
		},
		{
			"before": ["<C-k>"],
			"after": ["<C-w>", "k"]
		},
		{
			"before": ["<C-l>"],
			"after": ["<C-w>", "l"]
		}
	]
}
```

</details>
<br>
<br>

### Visual Mode

| Status             | Command      | Description                 |
| ------------------ | ------------ | --------------------------- |
| :white_check_mark: | `<leader>` l | Last Character In The Line  |
| :white_check_mark: | `<leader>` h | First Character In The Line |
| :white_check_mark: | J            | Move 5 Line Down            |
| :white_check_mark: | K            | Move 5 Line Up              |

<br>
<details>
 <summary><strong>Settings Example</strong> (click to expand)</summary>

Below is an example of a [settings.json](https://code.visualstudio.com/Docs/customization/userandworkspace) file with settings relevant to VSCodeVim:

```json
{
	"vim.visualModeKeyBindingsNonRecursive": [
		{
			"before": ["<Leader>", "l"],
			"after": ["$"]
		},
		{
			"before": ["<Leader>", "h"],
			"after": ["^"]
		},
		{
			"before": ["J"],
			"after": ["5", "j"]
		},
		{
			"before": ["K"],
			"after": ["5", "k"]
		}
	]
}
```

</details>
<br>
<br>

## VSCode Shortcuts

Visual Studio Code is a code editor redefined and optimized for building and debugging modern web and cloud applications.

### Normal Mode

| Status             | Command       | Description                |
| ------------------ | ------------- | -------------------------- |
| :white_check_mark: | `<leader>` ef | Focus On Files Explorer    |
| :white_check_mark: | `<leader>` a  | Source Action              |
| :white_check_mark: | `<leader>` sb | Toggle Side Bar Visibility |
| :white_check_mark: | `<leader>` ds | Duplicate Selection        |
| :white_check_mark: | `<leader>` fd | Format Document            |
| :white_check_mark: | `<leader>` q  | View Close Editor          |
| :white_check_mark: | `<leader>` w  | File Save                  |
| :white_check_mark: | `<leader>` r  | Rename Symbol              |
| :white_check_mark: | `<leader>` t  | Go To Symbol In Editor     |
| :white_check_mark: | `<leader>` u  | Transform To Title Case    |
| :white_check_mark: | `<leader>` i  | Toggle Editor Group Sizes  |
| :white_check_mark: | `<leader>` o  | Go To File In Editor       |
| :white_check_mark: | `<leader>` p  | Show All Commands          |
| :white_check_mark: | `<leader>` mn | Go To Next Problem         |
| :white_check_mark: | `<leader>` mN | Go To Previous Problem     |
| :white_check_mark: | `<leader>` tr | Tasks Rerun Last Task      |
| :white_check_mark: | `<leader>` tc | Tasks Configure Task       |

<br>
<details>
 <summary><strong>Settings Example</strong> (click to expand)</summary>

Below is an example of a [settings.json](https://code.visualstudio.com/Docs/customization/userandworkspace) file with settings relevant to VSCodeVim:

```json
{
	"vim.normalModeKeyBindingsNonRecursive": [
		{
			"before": ["<Leader>", "e", "f"],
			"commands": ["workbench.explorer.fileView.focus"]
		},
		{
			"before": ["<Leader>", "a"],
			"commands": ["editor.action.quickFix"]
		},
		{
			"before": ["<Leader>", "s", "b"],
			"commands": ["workbench.action.toggleSidebarVisibility"]
		},
		{
			"before": ["<Leader>", "d", "s"],
			"commands": ["editor.action.duplicateSelection"]
		},
		{
			"before": ["<Leader>", "f", "d"],
			"commands": ["editor.action.formatDocument"]
		},
		{
			"before": ["<Leader>", "q"],
			"commands": ["workbench.action.closeActiveEditor"]
		},
		{
			"before": ["<Leader>", "w"],
			"commands": ["workbench.action.files.save"]
		},
		{
			"before": ["<Leader>", "r"],
			"commands": ["editor.action.rename"]
		},
		{
			"before": ["<Leader>", "t"],
			"commands": ["workbench.action.gotoSymbol"]
		},
		{
			"before": ["<Leader>", "u"],
			"commands": ["editor.action.transformToTitlecase"]
		},
		{
			"before": ["<Leader>", "i"],
			"commands": ["workbench.action.toggleEditorWidths"]
		},
		{
			"before": ["<Leader>", "o"],
			"commands": ["workbench.action.quickOpen"]
		},
		{
			"before": ["<Leader>", "p"],
			"commands": ["workbench.action.showCommands"]
		},
		{
			"before": ["<Leader>", "m", "n"],
			"commands": ["editor.action.marker.next"]
		},
		{
			"before": ["<Leader>", "m", "N"],
			"commands": ["editor.action.marker.prev"]
		},
		{
			"before": ["<Leader>", "t", "r"],
			"commands": ["workbench.action.tasks.reRunTask"]
		},
		{
			"before": ["<Leader>", "t", "c"],
			"commands": ["workbench.action.tasks.configureTaskRunner"]
		}
	]
}
```

</details>
<br>
<br>

### Visual Mode

| Status             | Command      | Description                |
| ------------------ | ------------ | -------------------------- |
| :white_check_mark: | `<leader>` a | Source Action              |
| :white_check_mark: | `<leader>` s | Toggle Side Bar Visibility |
| :white_check_mark: | `<leader>` d | Duplicate Selection        |
| :white_check_mark: | `<leader>` f | Format Selection           |
| :white_check_mark: | `<leader>` u | Transform To Title Case    |
| :white_check_mark: | `<leader>` i | Toggle Editor Group Sizes  |
| :white_check_mark: | `<leader>` o | Go To File In Editor       |
| :white_check_mark: | `<leader>` p | Show All Commands          |
| :white_check_mark: | CTRL j       | Move Line Up               |
| :white_check_mark: | CTRL k       | Move Line Down             |

<br>
<details>
 <summary><strong>Settings Example</strong> (click to expand)</summary>

Below is an example of a [settings.json](https://code.visualstudio.com/Docs/customization/userandworkspace) file with settings relevant to VSCodeVim:

```json
{
	"vim.visualModeKeyBindingsNonRecursive": [
		{
			"before": ["<Leader>", "a"],
			"commands": ["editor.action.quickFix"]
		},
		{
			"before": ["<Leader>", "s"],
			"commands": ["workbench.action.toggleSidebarVisibility"]
		},
		{
			"before": ["<Leader>", "d"],
			"commands": ["editor.action.duplicateSelection"]
		},
		{
			"before": ["<Leader>", "f"],
			"commands": ["editor.action.formatSelection"]
		},
		{
			"before": ["<Leader>", "u"],
			"commands": ["editor.action.transformToTitlecase"]
		},
		{
			"before": ["<Leader>", "i"],
			"commands": ["workbench.action.toggleEditorWidths"]
		},
		{
			"before": ["<Leader>", "o"],
			"commands": ["workbench.action.quickOpen"]
		},
		{
			"before": ["<Leader>", "p"],
			"commands": ["workbench.action.showCommands"]
		},
		{
			"before": ["<C-j>"],
			"commands": ["editor.action.moveLinesDownAction"]
		},
		{
			"before": ["<C-k>"],
			"commands": ["editor.action.moveLinesUpAction"]
		}
	]
}
```

</details>
<br>
<br>

## View Commands

### Normal Mode

| Status             | Command        | Description                          |
| ------------------ | -------------- | ------------------------------------ |
| :white_check_mark: | `<leader>` vii | Increase Current View Size           |
| :white_check_mark: | `<leader>` vdd | Decrease Current View Size           |
| :white_check_mark: | `<leader>` vih | Increase Editor Height               |
| :white_check_mark: | `<leader>` vdh | Decrease Editor Height               |
| :white_check_mark: | `<leader>` viw | Increase Editor Width                |
| :white_check_mark: | `<leader>` vdw | Decrease Editor Width                |
| :white_check_mark: | `<leader>` tt  | File New Untitled File               |
| :white_check_mark: | `<leader>` tn  | View Open Next Editor                |
| :white_check_mark: | `<leader>` tN  | View Open Previous Editor            |
| :white_check_mark: | `<leader>` vgh | View Move Editor Group Left          |
| :white_check_mark: | `<leader>` vgj | View Move Editor Group Down          |
| :white_check_mark: | `<leader>` vgk | View Move Editor Group Up            |
| :white_check_mark: | `<leader>` vgl | View Move Editor Group Right         |
| :white_check_mark: | `<leader>` vif | View Move Editor Into First Group    |
| :white_check_mark: | `<leader>` vil | View Move Editor Into Last Group     |
| :white_check_mark: | `<leader>` vin | View Move Editor Into Next Group     |
| :white_check_mark: | `<leader>` vip | View Move Editor Into Previous Group |
| :white_check_mark: | `<leader>` veh | View Move Editor Left                |
| :white_check_mark: | `<leader>` vel | View Move Editor Right               |
| :white_check_mark: | `<leader>` ceg | View Close Editor Group              |
| :white_check_mark: | `<leader>` coe | View Close Other Editors In Group    |
| :white_check_mark: | `<leader>` ceo | View Close Editors In Other Groups   |
| :white_check_mark: | `<leader>` sh  | View Split Editor Left               |
| :white_check_mark: | `<leader>` sd  | View Split Editor Down               |
| :white_check_mark: | `<leader>` su  | View Split Editor Up                 |
| :white_check_mark: | `<leader>` sl  | View Split Editor Right              |

<br>
<details>
 <summary><strong>Settings Example</strong> (click to expand)</summary>

Below is an example of a [settings.json](https://code.visualstudio.com/Docs/customization/userandworkspace) file with settings relevant to VSCodeVim:

```json
{
	"vim.normalModeKeyBindingsNonRecursive": [
		{
			"before": ["<Leader>", "v", "i", "i"],
			"commands": ["workbench.action.increaseViewSize"]
		},
		{
			"before": ["<Leader>", "v", "d", "d"],
			"commands": ["workbench.action.decreaseViewSize"]
		},
		{
			"before": ["<Leader>", "v", "i", "h"],
			"commands": ["workbench.action.increaseViewHeight"]
		},
		{
			"before": ["<Leader>", "v", "d", "h"],
			"commands": ["workbench.action.decreaseViewHeight"]
		},
		{
			"before": ["<Leader>", "v", "i", "w"],
			"commands": ["workbench.action.increaseViewWidth"]
		},
		{
			"before": ["<Leader>", "v", "d", "w"],
			"commands": ["workbench.action.decreaseViewWidth"]
		},
		{
			"before": ["<Leader>", "t", "t"],
			"commands": ["workbench.action.files.newUntitledFile"]
		},
		{
			"before": ["<Leader>", "t", "n"],
			"commands": ["workbench.action.nextEditor"]
		},
		{
			"before": ["<Leader>", "t", "N"],
			"commands": ["workbench.action.previousEditor"]
		},
		{
			"before": ["<Leader>", "v", "g", "j"],
			"commands": ["workbench.action.moveActiveEditorGroupDown"]
		},
		{
			"before": ["<Leader>", "v", "g", "h"],
			"commands": ["workbench.action.moveActiveEditorGroupLeft"]
		},
		{
			"before": ["<Leader>", "v", "g", "l"],
			"commands": ["workbench.action.moveActiveEditorGroupRight"]
		},
		{
			"before": ["<Leader>", "v", "g", "k"],
			"commands": ["workbench.action.moveActiveEditorGroupUp"]
		},
		{
			"before": ["<Leader>", "v", "i", "f"],
			"commands": ["workbench.action.moveEditorToFirstGroup"]
		},
		{
			"before": ["<Leader>", "v", "i", "l"],
			"commands": ["workbench.action.moveEditorToLastGroup"]
		},
		{
			"before": ["<Leader>", "v", "i", "n"],
			"commands": ["workbench.action.moveEditorToNextGroup"]
		},
		{
			"before": ["<Leader>", "v", "i", "p"],
			"commands": ["workbench.action.moveEditorToPreviousGroup"]
		},
		{
			"before": ["<Leader>", "v", "e", "h"],
			"commands": ["workbench.action.moveEditorLeftInGroup"]
		},
		{
			"before": ["<Leader>", "v", "e", "l"],
			"commands": ["workbench.action.moveEditorRightInGroup"]
		},
		{
			"before": ["<Leader>", "c", "e", "g"],
			"commands": ["workbench.action.closeEditorsAndGroup"]
		},
		{
			"before": ["<Leader>", "c", "o", "e"],
			"commands": ["workbench.action.closeOtherEditors"]
		},
		{
			"before": ["<Leader>", "c", "e", "o"],
			"commands": ["workbench.action.closeEditorsInOtherGroups"]
		},
		{
			"before": ["<Leader>", "s", "h"],
			"commands": ["workbench.action.splitEditorLeft"]
		},
		{
			"before": ["<Leader>", "s", "d"],
			"commands": ["workbench.action.splitEditorDown"]
		},
		{
			"before": ["<Leader>", "s", "u"],
			"commands": ["workbench.action.splitEditorUp"]
		},
		{
			"before": ["<Leader>", "s", "r"],
			"commands": ["workbench.action.splitEditorRight"]
		}
	]
}
```

</details>
<br>
<br>

## Emmet Commands

Emmet allows you to write large HTML code blocks at speed of light using well-known CSS selectors. But it’s not the only thing that every web-developer needs: occasionally you have to edit your HTML and CSS code to fix bugs and add new features.

### Normal Mode

| Status             | Command        | Description                     |
| ------------------ | -------------- | ------------------------------- |
| :white_check_mark: | `<leader>` ei0 | Emmet Increment by 0.1          |
| :white_check_mark: | `<leader>` ed0 | Emmet Decrement by 0.1          |
| :white_check_mark: | `<leader>` eiu | Emmet Increment by 1            |
| :white_check_mark: | `<leader>` edu | Emmet Decrement by 1            |
| :white_check_mark: | `<leader>` eid | Emmet Increment by 10           |
| :white_check_mark: | `<leader>` edd | Emmet Decrement by 10           |
| :white_check_mark: | `<leader>` et  | Emmet Go To Matching Pair       |
| :white_check_mark: | `<leader>` en  | Emmet Go To Next Edit Point     |
| :white_check_mark: | `<leader>` eN  | Emmet Go To Previous Edit Point |
| :white_check_mark: | `<leader>` ex  | Emmet Evaluate Math Expression  |
| :white_check_mark: | `<leader>` eml | Emmet Merge Lines               |
| :white_check_mark: | `<leader>` eut | Emmet Update Tag                |
| :white_check_mark: | `<leader>` ert | Emmet Remove Tag                |
| :white_check_mark: | `<leader>` esj | Emmet Split / Join Tag          |
| :white_check_mark: | `<leader>` eui | Emmet Update Image Size         |
| :white_check_mark: | `<leader>` ec  | Emmet Toggle Comment            |
| :white_check_mark: | `<leader>` erc | Emmet Reflect CSS Value         |
| :white_check_mark: | `<leader>` ew  | Emmet Wrap with Abbreviation    |

<br>
<details>
 <summary><strong>Settings Example</strong> (click to expand)</summary>

Below is an example of a [settings.json](https://code.visualstudio.com/Docs/customization/userandworkspace) file with settings relevant to VSCodeVim:

```json
{
	"vim.normalModeKeyBindingsNonRecursive": [
		{
			"before": ["<Leader>", "e", "b", "i"],
			"commands": ["editor.emmet.action.balanceIn"]
		},
		{
			"before": ["<Leader>", "e", "b", "o"],
			"commands": ["editor.emmet.action.balanceOut"]
		},
		{
			"before": ["<Leader>", "e", "i", "0"],
			"commands": ["editor.emmet.action.incrementNumberByOneTenth"]
		},
		{
			"before": ["<Leader>", "e", "d", "0"],
			"commands": ["editor.emmet.action.decrementNumberByOneTenth"]
		},
		{
			"before": ["<Leader>", "e", "i", "u"],
			"commands": ["editor.emmet.action.incrementNumberByOne"]
		},
		{
			"before": ["<Leader>", "e", "d", "u"],
			"commands": ["editor.emmet.action.decrementNumberByOne"]
		},
		{
			"before": ["<Leader>", "e", "i", "d"],
			"commands": ["editor.emmet.action.incrementNumberByTen"]
		},
		{
			"before": ["<Leader>", "e", "d", "d"],
			"commands": ["editor.emmet.action.decrementNumberByTen"]
		},
		{
			"before": ["<Leader>", "e", "t"],
			"commands": ["editor.emmet.action.matchTag"]
		},
		{
			"before": ["<Leader>", "e", "n"],
			"commands": ["editor.emmet.action.nextEditPoint"]
		},
		{
			"before": ["<Leader>", "e", "N"],
			"commands": ["editor.emmet.action.prevEditPoint"]
		},
		{
			"before": ["<Leader>", "e", "x"],
			"commands": ["editor.emmet.action.evaluateMathExpression"]
		},
		{
			"before": ["<Leader>", "e", "m", "l"],
			"commands": ["editor.emmet.action.mergeLines"]
		},
		{
			"before": ["<Leader>", "e", "u", "t"],
			"commands": ["editor.emmet.action.updateTag"]
		},
		{
			"before": ["<Leader>", "e", "r", "t"],
			"commands": ["editor.emmet.action.removeTag"]
		},
		{
			"before": ["<Leader>", "e", "s", "j"],
			"commands": ["editor.emmet.action.splitJoinTag"]
		},
		{
			"before": ["<Leader>", "e", "u", "i"],
			"commands": ["editor.emmet.action.updateImageSize"]
		},
		{
			"before": ["<Leader>", "e", "c"],
			"commands": ["editor.emmet.action.toggleComment"]
		},
		{
			"before": ["<Leader>", "e", "r", "c"],
			"commands": ["editor.emmet.action.reflectCSSValue"]
		},
		{
			"before": ["<Leader>", "e", "w"],
			"commands": ["editor.emmet.action.wrapWithAbbreviation"]
		}
	]
}
```

</details>
<br>
<br>

### Visual Mode

| Status             | Command        | Description                                   |
| ------------------ | -------------- | --------------------------------------------- |
| :white_check_mark: | `<leader>` ebi | Emmet Balance (inward)                        |
| :white_check_mark: | `<leader>` ebo | Emmet Balance (outward)                       |
| :white_check_mark: | `<leader>` et  | Emmet Go To Matching Pair                     |
| :white_check_mark: | `<leader>` ec  | Emmet Toggle Comment                          |
| :white_check_mark: | `<leader>` en  | Emmet Select Next Item                        |
| :white_check_mark: | `<leader>` eN  | Emmet Select Previous Item                    |
| :white_check_mark: | `<leader>` ex  | Emmet Evaluate Math Expression                |
| :white_check_mark: | `<leader>` ew  | Emmet Wrap Individual Lines with Abbreviation |

<br>
<details>
 <summary><strong>Settings Example</strong> (click to expand)</summary>

Below is an example of a [settings.json](https://code.visualstudio.com/Docs/customization/userandworkspace) file with settings relevant to VSCodeVim:

```json
{
	"vim.visualModeKeyBindingsNonRecursive": [
		{
			"before": ["<Leader>", "e", "b", "i"],
			"commands": ["editor.emmet.action.balanceIn"]
		},
		{
			"before": ["<Leader>", "e", "b", "o"],
			"commands": ["editor.emmet.action.balanceOut"]
		},
		{
			"before": ["<Leader>", "e", "t"],
			"commands": ["editor.emmet.action.matchTag"]
		},
		{
			"before": ["<Leader>", "e", "c"],
			"commands": ["editor.emmet.action.toggleComment"]
		},
		{
			"before": ["<Leader>", "e", "n"],
			"commands": ["editor.emmet.action.selectNextItem"]
		},
		{
			"before": ["<Leader>", "e", "N"],
			"commands": ["editor.emmet.action.selectPrevItem"]
		},
		{
			"before": ["<Leader>", "e", "x"],
			"commands": ["editor.emmet.action.evaluateMathExpression"]
		},
		{
			"before": ["<Leader>", "e", "w"],
			"commands": [
				"editor.emmet.action.wrapIndividualLinesWithAbbreviation"
			]
		}
	]
}
```

</details>
<br>
<br>

## Git Commands

Git is a distributed version-control system for tracking changes in any set of files, originally designed for coordinating work among programmers cooperating on source code during software development. Its goals include speed, data integrity, and support for distributed, non-linear workflows.

### Normal Mode

| Status             | Command          | Description                             |
| ------------------ | ---------------- | --------------------------------------- |
| :white_check_mark: | `<leader>` gg    | Focus On Source Control View            |
| :white_check_mark: | `<leader>` gtl   | Focus On Timeline View                  |
| :white_check_mark: | `<leader>` gir   | Git Initialize Repository               |
| :white_check_mark: | `<leader>` gai   | Git Add To .gitignore                   |
| :white_check_mark: | `<leader>` gpg   | Publish To Github                       |
| :white_check_mark: | `<leader>` gar   | Git Add Remote                          |
| :white_check_mark: | `<leader>` grr   | Git Remove Remote                       |
| :white_check_mark: | `<leader>` gsc   | Git Stage Change                        |
| :white_check_mark: | `<leader>` gsac  | Git Stage All Changes                   |
| :white_check_mark: | `<leader>` gsamc | Git Stage All Merge Changes             |
| :white_check_mark: | `<leader>` gsatc | Git Stage All Tracked Changes           |
| :white_check_mark: | `<leader>` gsauc | Git Stage All Untracked Changes         |
| :white_check_mark: | `<leader>` guc   | Git Unstage Changes                     |
| :white_check_mark: | `<leader>` guac  | Git Unstage All Changes                 |
| :white_check_mark: | `<leader>` gcm   | Git Commit                              |
| :white_check_mark: | `<leader>` gca   | Git Commit All                          |
| :white_check_mark: | `<leader>` gcs   | Git Commit Staged                       |
| :white_check_mark: | `<leader>` gce   | Git Commit Empty                        |
| :white_check_mark: | `<leader>` gulc  | Git Undo Last Commit                    |
| :white_check_mark: | `<leader>` gp    | Git Push                                |
| :white_check_mark: | `<leader>` gpf   | Git Push (Force)                        |
| :white_check_mark: | `<leader>` gpbt  | Git Push To...                          |
| :white_check_mark: | `<leader>` gpbtf | Git Push To... (Force)                  |
| :white_check_mark: | `<leader>` gP    | Git Pull                                |
| :white_check_mark: | `<leader>` gPf   | Git Pull From...                        |
| :white_check_mark: | `<leader>` gPr   | Git Pull (Rebase)                       |
| :white_check_mark: | `<leader>` gAr   | Git Abort Rebase                        |
| :white_check_mark: | `<leader>` gcb   | Git Create Branch                       |
| :white_check_mark: | `<leader>` gcbf  | Git Create Branch From                  |
| :white_check_mark: | `<leader>` gdb   | Git Delete Branch                       |
| :white_check_mark: | `<leader>` gmb   | Git Merge Branch                        |
| :white_check_mark: | `<leader>` gpb   | Git Publish Branch                      |
| :white_check_mark: | `<leader>` grb   | Git Rename Branch                       |
| :white_check_mark: | `<leader>` gRb   | Git Rebase Branch                       |
| :white_check_mark: | `<leader>` gC    | Git Checkout To                         |
| :white_check_mark: | `<leader>` gCd   | Git Checkout To (Detached)              |
| :white_check_mark: | `<leader>` gcp   | Git Cherry Pick                         |
| :white_check_mark: | `<leader>` gdc   | Git Discard Changes                     |
| :white_check_mark: | `<leader>` gdac  | Git Discard All Changes                 |
| :white_check_mark: | `<leader>` gdatc | Git Discard All Tracked Changes         |
| :white_check_mark: | `<leader>` gdauc | Git Discard All Untracked Changes       |
| :white_check_mark: | `<leader>` gss   | Git Stash                               |
| :white_check_mark: | `<leader>` gsiu  | Git Stash (Include Untracked)           |
| :white_check_mark: | `<leader>` gas   | Git Apply Stash                         |
| :white_check_mark: | `<leader>` gals  | Git Apply Latest Stash                  |
| :white_check_mark: | `<leader>` gds   | Git Drop Stash                          |
| :white_check_mark: | `<leader>` gps   | Git Pop Stash                           |
| :white_check_mark: | `<leader>` gpls  | Git Pop Latest Stash                    |
| :white_check_mark: | `<leader>` gct   | Git Create Tag                          |
| :white_check_mark: | `<leader>` gdt   | Git Delete Tag                          |
| :white_check_mark: | `<leader>` gpt   | Git Push Tags                           |
| :white_check_mark: | `<leader>` gff   | Git Fetch                               |
| :white_check_mark: | `<leader>` gfp   | Git Fetch (Prune)                       |
| :white_check_mark: | `<leader>` gffar | Git Fetch From All Remotes              |
| :white_check_mark: | `<leader>` goc   | Git Open Changes                        |
| :white_check_mark: | `<leader>` gof   | Git Open File                           |
| :white_check_mark: | `<leader>` gsn   | Git Show Next Change                    |
| :white_check_mark: | `<leader>` gsN   | Git Show Previous Change                |
| :white_check_mark: | `<leader>` gmn   | Git Move To Next Change                 |
| :white_check_mark: | `<leader>` gmN   | Git Move To Previous Change             |
| :white_check_mark: | `<leader>` gcn   | Git Compare Editor Next Change          |
| :white_check_mark: | `<leader>` gcN   | Git Compare Editor Previous Change      |
| :white_check_mark: | `<leader>` giv   | Git Toggle Inline View                  |
| :white_check_mark: | `<leader>` mcb   | Merge Conflict Accept Both              |
| :white_check_mark: | `<leader>` mcc   | Merge Conflict Accept Current           |
| :white_check_mark: | `<leader>` mci   | Merge Conflict Accept Incoming          |
| :white_check_mark: | `<leader>` mcab  | Merge Conflict Accept All Both          |
| :white_check_mark: | `<leader>` mcac  | Merge Conflict Accept All Current       |
| :white_check_mark: | `<leader>` mcai  | Merge Conflict Accept All Incoming      |
| :white_check_mark: | `<leader>` mco   | Merge Conflict Compare Current Conflict |
| :white_check_mark: | `<leader>` mcn   | Merge Conflict Next Conflict            |
| :white_check_mark: | `<leader>` mcN   | Merge Conflict Previous Conflict        |

<br>
<details>
 <summary><strong>Settings Example</strong> (click to expand)</summary>

Below is an example of a [settings.json](https://code.visualstudio.com/Docs/customization/userandworkspace) file with settings relevant to VSCodeVim:

```json
{
	"vim.normalModeKeyBindingsNonRecursive": [
		{
			"before": ["leader", "g", "g"],
			"commands": ["workbench.scm.focus"]
		},
		{
			"before": ["leader", "g", "t", "l"],
			"commands": ["timeline.focus"]
		},
		{
			"before": ["leader", "g", "i", "r"],
			"commands": ["git.init"]
		},
		{
			"before": ["leader", "g", "a", "i"],
			"commands": ["git.ignore"]
		},
		{
			"before": ["leader", "g", "p", "g"],
			"commands": ["github.publish"]
		},
		{
			"before": ["leader", "g", "a", "r"],
			"commands": ["git.addRemote"]
		},
		{
			"before": ["leader", "g", "r", "r"],
			"commands": ["git.removeRemote"]
		},
		{
			"before": ["leader", "g", "s", "c"],
			"commands": ["git.stage"]
		},
		{
			"before": ["leader", "g", "s", "a", "c"],
			"commands": ["git.stageAll"]
		},
		{
			"before": ["leader", "g", "s", "a", "m", "c"],
			"commands": ["git.stageAllMerge"]
		},
		{
			"before": ["leader", "g", "s", "a", "t", "c"],
			"commands": ["git.stageAllTracked"]
		},
		{
			"before": ["leader", "g", "s", "a", "t", "c"],
			"commands": ["git.stageAllUntracked"]
		},
		{
			"before": ["leader", "g", "u", "c"],
			"commands": ["git.unstage"]
		},
		{
			"before": ["leader", "g", "u", "a", "c"],
			"commands": ["git.unstageAll"]
		},
		{
			"before": ["leader", "g", "c", "c"],
			"commands": ["git.commit"]
		},
		{
			"before": ["leader", "g", "c", "a"],
			"commands": ["git.commitAll"]
		},
		{
			"before": ["leader", "g", "c", "s"],
			"commands": ["git.commitStaged"]
		},
		{
			"before": ["leader", "g", "c", "e"],
			"commands": ["git.commitEmpty"]
		},
		{
			"before": ["leader", "g", "u", "l", "c"],
			"commands": ["git.undoCommit"]
		},
		{
			"before": ["leader", "g", "p"],
			"commands": ["git.push"]
		},
		{
			"before": ["leader", "g", "p", "f"],
			"commands": ["git.pushForce"]
		},
		{
			"before": ["leader", "g", "p", "b", "t"],
			"commands": ["git.pushTo"]
		},
		{
			"before": ["leader", "g", "p", "b", "t", "f"],
			"commands": ["git.pushToForce"]
		},
		{
			"before": ["leader", "g", "P"],
			"commands": ["git.pull"]
		},
		{
			"before": ["leader", "g", "P", "f"],
			"commands": ["git.pullFrom"]
		},
		{
			"before": ["leader", "g", "P", "r"],
			"commands": ["git.pullRebase"]
		},
		{
			"before": ["leader", "g", "A", "r"],
			"commands": ["git.rebaseAbort"]
		},
		{
			"before": ["leader", "g", "c", "b"],
			"commands": ["git.branch"]
		},
		{
			"before": ["leader", "g", "c", "b", "f"],
			"commands": ["git.branchFrom"]
		},
		{
			"before": ["leader", "g", "d", "b"],
			"commands": ["git.deleteBranch"]
		},
		{
			"before": ["leader", "g", "m", "b"],
			"commands": ["git.merge"]
		},
		{
			"before": ["leader", "g", "p", "b"],
			"commands": ["git.publish"]
		},
		{
			"before": ["leader", "g", "r", "b"],
			"commands": ["git.renameBranch"]
		},
		{
			"before": ["leader", "g", "R", "b"],
			"commands": ["git.rebase"]
		},
		{
			"before": ["leader", "g", "C"],
			"commands": ["git.checkout"]
		},
		{
			"before": ["leader", "g", "C", "d"],
			"commands": ["git.checkoutDetached"]
		},
		{
			"before": ["leader", "g", "c", "p"],
			"commands": ["git.cherryPick"]
		},
		{
			"before": ["leader", "g", "d", "c"],
			"commands": ["git.clean"]
		},
		{
			"before": ["leader", "g", "d", "a", "c"],
			"commands": ["git.cleanAll"]
		},
		{
			"before": ["leader", "g", "d", "a", "t", "c"],
			"commands": ["git.cleanAllTracked"]
		},
		{
			"before": ["leader", "g", "d", "a", "u", "c"],
			"commands": ["git.cleanAllUntracked"]
		},
		{
			"before": ["leader", "g", "s", "s"],
			"commands": ["git.stash"]
		},
		{
			"before": ["leader", "g", "s", "i", "u"],
			"commands": ["git.stashIncludeUntracked"]
		},
		{
			"before": ["leader", "g", "a", "s"],
			"commands": ["git.stashApply"]
		},
		{
			"before": ["leader", "g", "a", "l", "s"],
			"commands": ["git.stashApplyLatest"]
		},
		{
			"before": ["leader", "g", "d", "s"],
			"commands": ["git.stashDrop"]
		},
		{
			"before": ["leader", "g", "p", "s"],
			"commands": ["git.stashPop"]
		},
		{
			"before": ["leader", "g", "p", "l", "s"],
			"commands": ["git.stashPopLatest"]
		},
		{
			"before": ["leader", "g", "c", "t"],
			"commands": ["git.createTag"]
		},
		{
			"before": ["leader", "g", "d", "t"],
			"commands": ["git.deleteTag"]
		},
		{
			"before": ["leader", "g", "p", "t"],
			"commands": ["git.pushTags"]
		},
		{
			"before": ["leader", "g", "f", "f"],
			"commands": ["git.fetch"]
		},
		{
			"before": ["leader", "g", "f", "p"],
			"commands": ["git.fetchPrune"]
		},
		{
			"before": ["leader", "g", "f", "f", "a", "r"],
			"commands": ["git.fetchAll"]
		},
		{
			"before": ["leader", "g", "o", "c"],
			"commands": ["git.openChange"]
		},
		{
			"before": ["leader", "g", "o", "f"],
			"commands": ["git.openFile"]
		},
		{
			"before": ["leader", "g", "s", "n"],
			"commands": ["editor.action.dirtydiff.next"]
		},
		{
			"before": ["leader", "g", "s", "N"],
			"commands": ["editor.action.dirtydiff.previous"]
		},
		{
			"before": ["leader", "g", "m", "n"],
			"commands": ["workbench.action.editor.nextChange"]
		},
		{
			"before": ["leader", "g", "m", "N"],
			"commands": ["workbench.action.editor.previousChange"]
		},
		{
			"before": ["leader", "g", "c", "n"],
			"commands": ["workbench.action.compareEditor.nextChange"]
		},
		{
			"before": ["leader", "g", "c", "N"],
			"commands": ["workbench.action.compareEditor.previousChange"]
		},
		{
			"before": ["leader", "g", "i", "v"],
			"commands": ["toggle.diff.renderSideBySide"]
		},
		{
			"before": ["leader", "m", "c", "b"],
			"commands": ["merge-conflict.accept.both"]
		},
		{
			"before": ["leader", "m", "c", "c"],
			"commands": ["merge-conflict.accept.current"]
		},
		{
			"before": ["leader", "m", "c", "i"],
			"commands": ["merge-conflict.accept.incoming"]
		},
		{
			"before": ["leader", "m", "c", "a", "b"],
			"commands": ["merge-conflict.accept.all-both"]
		},
		{
			"before": ["leader", "m", "c", "a", "c"],
			"commands": ["merge-conflict.accept.all-current"]
		},
		{
			"before": ["leader", "m", "c", "a", "i"],
			"commands": ["merge-conflict.accept.all-incoming"]
		},
		{
			"before": ["leader", "m", "c", "o"],
			"commands": ["merge-conflict.compare"]
		},
		{
			"before": ["leader", "m", "c", "n"],
			"commands": ["merge-conflict.next"]
		},
		{
			"before": ["leader", "m", "c", "N"],
			"commands": ["merge-conflict.previous"]
		}
	]
}
```

</details>
<br>
<br>

### Visual Mode

| Status             | Command        | Description                     |
| ------------------ | -------------- | ------------------------------- |
| :white_check_mark: | `<leader>` gs  | Git Stage Selected Ranges       |
| :white_check_mark: | `<leader>` gu  | Git Unstage Selected Ranges     |
| :white_check_mark: | `<leader>` gr  | Git Revert Selected Ranges      |
| :white_check_mark: | `<leader>` mca | Merge Conflict Accept Selection |

<br>
<details>
 <summary><strong>Settings Example</strong> (click to expand)</summary>

Below is an example of a [settings.json](https://code.visualstudio.com/Docs/customization/userandworkspace) file with settings relevant to VSCodeVim:

```json
{
	"vim.visualModeKeyBindingsNonRecursive": [
		{
			"before": ["<Leader>", "g", "s"],
			"commands": ["git.stageSelectedRanges"]
		},
		{
			"before": ["<Leader>", "g", "u"],
			"commands": ["git.unstageSelectedRanges"]
		},
		{
			"before": ["<Leader>", "g", "r"],
			"commands": ["git.revertSelectedRanges"]
		},
		{
			"before": ["leader", "m", "c", "a"],
			"commands": ["merge-conflict.accept.selection"]
		}
	]
}
```

</details>
<br>
<br>

## Debug Commands

### Normal Mode

| Status             | Command        | Description                      |
| ------------------ | -------------- | -------------------------------- |
| :white_check_mark: | `<leader>` df  | View Show Run And Debug          |
| :white_check_mark: | `<leader>` dc  | Debug Continue                   |
| :white_check_mark: | `<leader>` dp  | Debug Pause                      |
| :white_check_mark: | `<leader>` dr  | Debug Restart                    |
| :white_check_mark: | `<leader>` dh  | Debug Show Hover                 |
| :white_check_mark: | `<leader>` ds  | Debug Start Debugging            |
| :white_check_mark: | `<leader>` di  | Debug Step Into                  |
| :white_check_mark: | `<leader>` du  | Debug Step Out                   |
| :white_check_mark: | `<leader>` do  | Debug Step Over                  |
| :white_check_mark: | `<leader>` dx  | Debug Stop                       |
| :white_check_mark: | `<leader>` db  | Debug Toggle Breakpoint          |
| :white_check_mark: | `<leader>` dal | Debug Add Logpoint               |
| :white_check_mark: | `<leader>` daf | Debug Add Function Breakpoint    |
| :white_check_mark: | `<leader>` dac | Debug Add Conditional Breakpoint |
| :white_check_mark: | `<leader>` dai | Debug Inline Breakpoint          |
| :white_check_mark: | `<leader>` deb | Debug Enable All Breakpoint      |
| :white_check_mark: | `<leader>` ddb | Debug Disable All Breakpoint     |
| :white_check_mark: | `<leader>` drb | Debug Remove All Breakpoint      |
| :white_check_mark: | `<leader>` dn  | Debug Go To Next Breakpoint      |
| :white_check_mark: | `<leader>` dN  | Debug Go To Previous Breakpoint  |

<br>
<details>
 <summary><strong>Settings Example</strong> (click to expand)</summary>

Below is an example of a [settings.json](https://code.visualstudio.com/Docs/customization/userandworkspace) file with settings relevant to VSCodeVim:

```json
{
	"vim.normalModeKeyBindingsNonRecursive": [
		{
			"before": ["<Leader>", "d", "f"],
			"commands": ["workbench.view.debug"]
		},
		{
			"before": ["<Leader>", "d", "c"],
			"commands": ["workbench.action.debug.continue"]
		},
		{
			"before": ["<Leader>", "d", "p"],
			"commands": ["workbench.action.debug.pause"]
		},
		{
			"before": ["<Leader>", "d", "r"],
			"commands": ["workbench.action.debug.restart"]
		},
		{
			"before": ["<Leader>", "d", "h"],
			"commands": ["editor.debug.action.showDebugHover"]
		},
		{
			"before": ["<Leader>", "d", "s"],
			"commands": ["workbench.action.debug.start"]
		},
		{
			"before": ["<Leader>", "d", "i"],
			"commands": ["workbench.action.debug.stepInto"]
		},
		{
			"before": ["<Leader>", "d", "u"],
			"commands": ["workbench.action.debug.stepOut"]
		},
		{
			"before": ["<Leader>", "d", "o"],
			"commands": ["workbench.action.debug.stepOver"]
		},
		{
			"before": ["<Leader>", "d", "b"],
			"commands": ["editor.debug.action.toggleBreakpoint"]
		},
		{
			"before": ["<Leader>", "d", "a", "l"],
			"commands": ["editor.debug.action.addLogPoint"]
		},
		{
			"before": ["<Leader>", "d", "a", "f"],
			"commands": [
				"workbench.debug.viewlet.action.addFunctionBreakpointAction"
			]
		},
		{
			"before": ["<Leader>", "d", "a", "c"],
			"commands": ["editor.debug.action.conditionalBreakpoint"]
		},
		{
			"before": ["<Leader>", "d", "a", "i"],
			"commands": ["editor.debug.action.toggleInlineBreakpoint"]
		},
		{
			"before": ["<Leader>", "d", "e", "b"],
			"commands": ["workbench.debug.viewlet.action.enableAllBreakpoints"]
		},
		{
			"before": ["<Leader>", "d", "d", "b"],
			"commands": ["workbench.debug.viewlet.action.disableAllBreakpoints"]
		},
		{
			"before": ["<Leader>", "d", "r", "b"],
			"commands": ["workbench.debug.viewlet.action.removeAllBreakpoints"]
		},
		{
			"before": ["<Leader>", "d", "n"],
			"commands": ["editor.debug.action.goToNextBreakpoint"]
		},
		{
			"before": ["<Leader>", "d", "N"],
			"commands": ["editor.debug.action.goToPreviousBreakpoint"]
		}
	]
}
```

</details>
<br>
<br>
