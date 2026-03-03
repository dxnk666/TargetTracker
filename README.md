# Target Tracker

A desktop application for tracking targets in Chivalry 2, built with WPF and backed by a centralized database.

---

## Features

- Automatically detects targets on your current server
- Centralized database shared across all users in real-time
- Role-based access control (User, Veteran, Admin, SuperAdmin)
- Automatic update system

---

## Installation

1. Download the latest `TargetTracker.exe` from the [Releases](https://github.com/dxnk666/TargetTracker/releases) page
2. Run the exe — no installation required
3. Log in with your credentials

> Your settings are saved to `C:\Users\<you>\AppData\Roaming\TargetTracker\`

---

## How to Use

### Targets Page

This is the main page. It shows which targets are currently on your server.

1. Open Chivalry 2 and join a server
2. Click **Find Targets on This Server**
3. The app will automatically run `listplayers` in the game console and compare the results with the target list
4. Any matches will appear in the table with their current name, saved name, tier, note, and who added them

> Make sure your console keybind in the app matches the one set in Chivalry 2 (default: F2)

---

### Edit Page

This page is for managing the target list. Only **Veteran**, **Admin** roles can access this page.

#### Quick Add from Server
1. Click **Refresh** to load players currently on your server
2. Select a player from the dropdown
3. Optionally enter a **Tier** (1–5)
4. Click **Quick Add**

#### Manual Add
1. Paste player data into the text box (format: `Name - PlayFabID`)
2. Optionally fill in **Note** and **Tier**
3. Click **+ Add**

> You can paste multiple lines at once to add multiple targets

#### Edit an Existing Target
1. Double-click a row in the list
2. Modify the fields (including Tier and Note)
3. Click **Update**
4. Click **Cancel** to discard changes

#### Remove a Target
1. Select a row in the list
2. Click **Remove**
3. Confirm the deletion

---

### Settings Page

#### Console Keybind
- Click **Change Key** and press any key to set your console keybind
- This must match the key that opens the console in Chivalry 2

#### Account
- Click **Change Password** to update your password

---

## Tier System

Tiers are optional labels you can assign to targets to indicate priority or threat level.

> Tiers are purely informational. there's no enforced meaning. Use them in whatever way helps your team the most.

---

## Admin Panel

Accessible from Settings → Admin Panel

### User List
- Shows all registered users with their username and role

### Change Role
1. Select a user from the list
2. Choose a role from the dropdown (User, Veteran, Admin)
3. Click **Change Role**

### Delete User
1. Select a user from the list
2. Click **Delete User**
3. Confirm the deletion

### Add New User
1. Enter a username and password
2. Select a role
3. Click **+ Add User**

---

## Roles

| Role | Permissions |
|---|---|
| User | View targets only, cannot access Edit page |
| Veteran | Add, edit, and delete own targets |
| Admin | Full target management + user management |

---

## Troubleshooting

**"Chivalry 2 not found"**
→ Make sure Chivalry 2 is running before clicking Find Targets

**"Data cannot be retrieved from the game"**
→ Check that your console keybind in the app matches the one in-game

**"Unable to connect to the server"**
→ The API may be starting up. Wait a moment and try again.

**Targets not updating**
→ The list auto-refreshes every 10 seconds. You can also switch pages to force a refresh.
