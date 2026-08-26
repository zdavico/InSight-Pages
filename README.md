# InSight HTML Pages

This repository contains the HTML pages for the InSight program at Champlain College's Career Collaborative. Pages are
edited using [Phoenix Code](https://phcode.io/) with its built-in live preview and Git integration.

## Getting Started

### First-time setup

Clone the repository to your local machine:

```bash
git clone https://github.com/zdavico/InSight-Pages.git
```

Open the cloned folder as a project in Phoenix Code. The Git panel in the sidebar will automatically detect the repo.

### Editor setup

Phoenix Code's Git integration handles most of the workflow visually, but the built-in terminal is available for
anything the panel doesn't cover. To confirm Git is enabled, go to Settings and check that "Enable Git" is toggled on.

## Daily Workflow

### Before you start editing

Always pull the latest changes before you begin working. This ensures you have your collaborator's most recent updates
and avoids merge conflicts.

**From the Phoenix Code Git panel:** Click the sync/pull button to fetch and merge remote changes.

**From the terminal:**

```bash
git pull origin main
```

### Making and saving edits

1. Edit your HTML files as usual. Modified files will appear highlighted in the file tree and listed in the Git panel.
2. When you're ready to save your work to the repo, **stage** your changes by selecting the files in the Git panel (or
   stage all).
3. Write a short, descriptive **commit message** that explains what you changed (e.g., "Updated Year 2 milestone page
   layout" or "Added FastPass Day announcement for Spring").
4. Click **Commit**.

**From the terminal:**

```bash
git add .
git commit -m "Your commit message here"
```

Note: I'm not a stickler for message commit syntax, so it can be super casual. For example: "updated CT, MT, PL and YR3
home" or something like that.

### Pushing your changes

After committing, push your changes so Zeke can access them.

**From the Phoenix Code Git panel:** Click the sync/push button.

**From the terminal:**

```bash
git push origin main
```

### Quick reference: the full cycle

```
pull → edit → stage → commit → push
```

Every session should start with a pull and end with a push.

## Handling Merge Conflicts

If you and Iedit the same lines in the same file, Git will flag a merge conflict when you pull. When this happens:

1. Open the conflicting file. Git marks the conflicts with `<<<<<<<`, `=======`, and `>>>>>>>` markers.
2. Edit the file to keep the correct version (or combine both changes).
3. Remove the conflict markers.
4. Stage the resolved file, commit, and push.

The simplest way to avoid conflicts is to communicate about which files you're each working on and pull frequently. I
will avoid pushing/pulling during your work hours, and you can refrain from modifying these outside your InSight
Coordinator hours. If you do, for any reason, need to push updates outside those hours (forgot to push, needed to fix
something) I think that will be OK, just Gchat me beforehand.

If we do end up in a situation where a conflict is flagged, abort the push and avoid running the pull command until we
get on the same page.

If we accidentally merge conflicting files, there's a way to trace back changes. Not the end of the world, but not the
most fun task with html files.

## Tips

-   **Commit often.** Small, frequent commits are easier to understand and easier to undo if something breaks.
-   **Write clear commit messages.** Future you will thank present you.
-   **Pull before you push.** If your collaborator has pushed changes since your last pull, Git will ask you to pull
    first anyway.
-   **Use branches for big changes.** If you're reworking a page significantly, consider creating a branch
    (`git checkout -b your-branch-name`) so the main version stays stable while you work.