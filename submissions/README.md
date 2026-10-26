# Acceptance evidence

| File | What it shows |
| --- | --- |
| `task1-running.png` | The complete application window running locally. |
| `task2-description.png` | The actual Modify furniture view with the edited description, after saving and reopening the home. |
| `task3-volume.png` | The actual furniture table populated with calculated volumes in ascending order, alongside the application's Sort by menu containing Volume. |
| `task4-all-levels.pdf` | Output from the application's PDF printer: an all-level furniture table with a Level column, followed by the plans for Level 0, Level 1, and Level 2. |

The Task 2 and Task 3 PNGs are component renderings produced from the modified application's Java Swing views by a local verification harness, using English labels and the standard cross-platform Swing look and feel. Their captions identify this verification method.

## Local verification

- All six provided Maven tests pass, with no failures, errors, or skipped tests.
- `test_submission.py` passes the submission structure check.
- Description edits propagate from the text field to the controller and furniture object, survive a `.sh3d` save/reopen, and appear in the reopened editor.
- Volume is calculated for catalog and home furniture, appears by default in a new home, sorts in both directions, and updates and reorders the table when dimensions change.
- Volume sort and display controls are present in both the main and context menus, with enabled actions and tooltip text.
- Printing produces four pages for the supplied sample. The furniture group is expanded in this output so its child furniture is also listed.
- Printing preserves the original selected level and on-screen Level column setting. Local checks also cover rendering/printer failures, hidden levels, an empty level, fixed-scale multi-page plans, and homes without explicit levels.
- The four output pages were rendered and visually reviewed, including furniture names, level labels, and each level's plan.
