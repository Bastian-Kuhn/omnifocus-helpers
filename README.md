# Omnifocus Plugin Collection

Here I collect small plugins and helpers I build and use with OmniFocus.

In separate Repos you find:

- [Jira to OmniFocus](https://github.com/Bastian-Kuhn/jira-omnifocus)
- [Zammad to OmniFocus](https://github.com/Bastian-Kuhn/zammad-omnifocus)

In this Repo:

## Obsidian Project

Opens or creates an Obsidian note whose name matches the selected OmniFocus task or project.

- If the note already exists it is opened unchanged.
- If the note does not exist it is created as a new empty note.
- Uses `obsidian://new?append=true` to avoid duplicate numbered files.

**Configuration** (top of the script):

| Constant | Default | Description |
|---|---|---|
| `OBSIDIAN_VAULT_NAME` | `"Notes"` | Vault name or vault ID. Leave empty to use the last active vault. |
| `OBSIDIAN_FOLDER_PATH` | `"02 - Projects/"` | Target folder path inside the vault. Supports nested paths, e.g. `Projects/OmniFocus`. |

**Install:**
```
cp obsidian-project.omnifocusjs ~/Library/Containers/com.omnigroup.OmniFocus4/Data/Library/Application\ Support/Plug-Ins/
```


## Agenda Project

Opens or creates an Agenda project whose title matches the selected OmniFocus task or project.

- Tries `agenda://x-callback-url/open-project` first.
- Falls back to `agenda://x-callback-url/create-project` on error 404.

**Install:**
```
cp agenda-project.omnifocusjs ~/Library/Containers/com.omnigroup.OmniFocus4/Data/Library/Application\ Support/Plug-Ins/
```


## Task E-Mail

Opens a pre-filled email draft for the selected task or project. Recipients are pulled from tags that are children of a configurable tag group (default: `Ansprechpartner`). Hold **Option** when triggering the action to change the tag group name.

**Install:**
```
cp task-email.omnifocusjs ~/Library/Containers/com.omnigroup.OmniFocus4/Data/Library/Application\ Support/Plug-Ins/
```
