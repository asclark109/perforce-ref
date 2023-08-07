# Perforce
https://www.youtube.com/watch?v=Yvgxx2vwsRY&list=PLxdnSsBqCrrGq_8ecmdE7A6KnRfbhHE4Q&index=1

## Getting Started
https://www.youtube.com/watch?v=Yvgxx2vwsRY&list=PLxdnSsBqCrrGq_8ecmdE7A6KnRfbhHE4Q&index=1&pp=iAQB

Centralized Version Control System
- files maintained on a central server
- files are organized into _depots_
  - __depot__: basically a folder which can contain other folders and files
  - 1 depot per project (_typically_)

__workspace__: defines which files to download to local machine from the perforce server
- it is just a mapping of files on the server to download
- workspace definitions are stored on the perforce server
- can be updated / modified after creating

> _perforce server_ has _depots_ and _workspace_ definitions; _workspaces_ may map to multiple depots/files

### Setting Up P4v

### Creating a Workspace

_notable things in the perforce UI_
- __pending changelists__: see the 
- __submitted changelists__: see the commits of others

create a directory to hold the perforce workspace ("sandbox")

---

## Basic Operations with Perforce
https://www.youtube.com/watch?v=_5_LK_0H22I&list=PLxdnSsBqCrrGq_8ecmdE7A6KnRfbhHE4Q&index=2&pp=iAQB

1. startup p4v; (type p4v in linux console?)
2. browse workspace and select one; new UI will pop up for the workspace

3. look in the bottom left corner to see if any files in your workspace have been updated
- can see the since submitted changelists and what files changed (can update your files)

### making changes to files

__changelist__: describes what you're trying to change 

1. create a _changelist_. 
2. checking out files
3. modifying files
4. submit changelist, which pushes the changes back to the server (modification of files, creation of new files, deletion of files).

---

## Deleting a Perforce Workspace from a machine
https://www.youtube.com/watch?v=dHMXgDzV1Hc&list=PLxdnSsBqCrrGq_8ecmdE7A6KnRfbhHE4Q&index=4

Remember, there is a two way street between the workspace and the perforce server
1. open p4v. go to `view -> workspaces` (go to `workspaces` tab)
2. `right-click` on the specific workspace and click `Delete Workspace '<myworkspace>'`
> note: this only deletes the mapping (the link) between files on the server and your computer
3. After the workspace is deleted from the server, you can just delete the files locally on the computer

---

## Adding and Deleting Users on a Perforce Server
https://www.youtube.com/watch?v=h9WCEvbu5JI&list=PLxdnSsBqCrrGq_8ecmdE7A6KnRfbhHE4Q&index=6

_requires opening p4v admin, which requires a login with an admin role_

---

## Creating and Initializing a New Perforce Depot
https://www.youtube.com/watch?v=pv4tvwghGCQ&list=PLxdnSsBqCrrGq_8ecmdE7A6KnRfbhHE4Q&index=7&pp=iAQB

_requires opening p4v admin, which requires a login with an admin role_

---

| IDE with versioning plug-in | Other commonly used terms | Corresponding Perforce command |
|---|---|---|
| Add to source control/Perforce | Add | p4 add |
| Check out | Edit | p4 edit |
| Check in | Submit | p4 submit |
| Show differences | Diff | p4 diff |
| Get latest version | Sync, Refresh | p4 sync |
| Show history | Filelog | p4 filelog |
| Undo checkout | Revert | p4 revert |
| Remove from source control | Delete | p4 delete |

| Task | Description | Perforce activity |
|---|---|---|
| Add files to the depot | After you add files to your project, you add them to the depot. | Files are opened for add in a pending changelist. |
| Retrieve files | Get a copy of a file from the depot. | Files are synced to your computer. |
| Check files out | Get the latest version from the depot for editing. | Files are opened for edit in a pending changelist. |
| Check files in | Put your edited files in the depot as the most recent revisions. | A pending changelist is submitted. |
| Diff files | Compare a file with a previous revision to see what's changed. | The Perforce diff utility is launched to display differences between two versions of a file. |
| Revert files | Discard changes you've made to your local copy of a depot file. | The head revision is synced to your client workspace and removed from its pending changelist. |
| Delete files | Remove a file from a project and from the depot. | Files are opened for delete in a pending changelist. |

---

Command line guide: https://www.perforce.com/manuals/p4guide/Content/P4Guide/Home-p4guide.html