# Setup Guide: do this BEFORE Class 1

Please finish this guide at home before our first class. It takes about **45–60 minutes**.
If you get stuck, write down the step and the error message (or take a screenshot), and we'll fix it together at the start of class.

**You need:** your own laptop (Windows or macOS), admin rights to install software, about 3 GB of free space, and internet.

| # | Tool | What it's for | First used |
|---|---|---|---|
| 1 | GitHub account | Storing and sharing your code online | Class 1 |
| 2 | VS Code | The code editor we write everything in | Class 1 |
| 3 | Git | Tracks changes to your code; downloads the lab files | Class 1 |
| 4 | XAMPP (or MAMP on Mac) | Runs a web server, PHP and MySQL on your laptop | Class 5 (install it now anyway) |
| 5 | Lab files | Your own copy of this repository | Class 1 |

---

## Step 0 (Windows only): show file extensions

If you skip this, files can secretly end up named `index.html.txt`.

1. Open **File Explorer**.
2. Windows 11: **View → Show → File name extensions** (make sure it's ticked).
   Windows 10: **View** tab → tick **File name extensions**.

---

## Step 1: Create a GitHub account

1. Go to <https://github.com/signup> and create a free account.
2. Use an email you will keep using, and remember your **username**.

---

## Step 2: Install VS Code

Download from <https://code.visualstudio.com>.

**Windows**
1. Run the installer.
2. On the "Select Additional Tasks" screen, tick:
   - **Add "Open with Code" action to Windows Explorer file context menu**
   - **Add "Open with Code" action to Windows Explorer directory context menu**
   - **Add to PATH** (usually ticked already)

**macOS**
1. Open the downloaded `.zip` file.
2. Drag **Visual Studio Code.app** into your **Applications** folder. Don't run it from Downloads.
3. Open VS Code from Applications.

**Both: install these extensions**

Click the Extensions icon in the left sidebar (four squares), search for each one and click **Install**:

| Extension | Publisher | Why |
|---|---|---|
| **Live Server** | Ritwick Dey | Opens your page in the browser and refreshes it automatically when you save |
| **Prettier - Code formatter** | Prettier | Tidies up your code formatting |
| **PHP Intelephense** | Ben Mewburn | PHP help, from Class 5 onwards |

**Both: turn on Auto Save** with **File → Auto Save** (a tick appears). This avoids the classic "I changed it but nothing happened!" problem.

---

## Step 3: Install Git

**Windows**
1. Download from <https://git-scm.com/download/win> and run the installer.
2. The default options are fine, with two changes:
   - "Choosing the default editor": pick **Use Visual Studio Code as Git's default editor**.
   - "Adjusting the name of the initial branch": pick **Override** and type `main`.

**macOS**
1. Open the **Terminal** app (press Cmd + Space, type "Terminal").
2. Type `git --version` and press Enter.
3. If Git isn't installed, a popup offers to install the **Command Line Developer Tools**. Click **Install** and wait for it to finish.

**Both: tell Git who you are**

Open a terminal (in VS Code: **Terminal → New Terminal**) and run these two commands, using your own name and the **same email as your GitHub account**:

```bash
git config --global user.name "Your Name"
```

```bash
git config --global user.email "you@example.com"
```

Check it worked:

```bash
git config --global --list
```

You should see your name and email.

---

## Step 4: Install XAMPP (Apache + PHP + MySQL)

We won't use this until Class 5, but install it now so any problems get fixed early.

Download from <https://www.apachefriends.org> (choose the newest PHP 8 version for your system).

### Windows

1. Run the installer. If you see a warning about **UAC / User Account Control**, click **OK**.
2. Keep the default components and the default folder **`C:\xampp`**. Don't install it in "Program Files".
3. When it finishes, open the **XAMPP Control Panel**.
4. Click **Start** next to **Apache** and **MySQL**. Both names should turn **green**.
5. If Windows Firewall asks, click **Allow access**.
6. Open your browser and go to <http://localhost>. You should see the XAMPP welcome page.

### macOS

1. Open the downloaded `.dmg` file and run the installer.
   If macOS says it *"can't be opened"*, go to **System Settings → Privacy & Security**, scroll down and click **Open Anyway**.
2. Open **Applications → XAMPP → manager-osx** (it may be called "XAMPP" or "manager-osx").
3. Go to the **Manage Servers** tab and click **Start All**. Apache and MySQL should show **Running**.
4. Open your browser and go to <http://localhost>.

> **XAMPP not working on your Mac?** This sometimes happens on newer Macs (M1/M2/M3/M4).
> Use **MAMP** instead. It does the same job.
> 1. Download the free version from <https://www.mamp.info>.
> 2. The installer adds both **MAMP** and **MAMP PRO**. Use plain **MAMP** (PRO is a paid trial).
> 3. Open MAMP and click **Start**. Your website address is <http://localhost:8888>.

### Where things are (keep this table!)

| | XAMPP on Windows | XAMPP on macOS | MAMP on macOS |
|---|---|---|---|
| Web folder ("htdocs") | `C:\xampp\htdocs` | `/Applications/XAMPP/xamppfiles/htdocs` | `/Applications/MAMP/htdocs` |
| Website address | <http://localhost> | <http://localhost> | <http://localhost:8888> |
| phpMyAdmin (database tool) | <http://localhost/phpmyadmin> | <http://localhost/phpmyadmin> | Open from the MAMP start page |
| MySQL username / password | `root` / *(empty)* | `root` / *(empty)* | `root` / `root` |

### Test that PHP works

1. In VS Code: **File → Open Folder** and open your **htdocs** folder (see the table above).
2. Create a new file called `test.php` containing:
   ```php
   <?php echo "PHP is working!"; ?>
   ```
3. Visit <http://localhost/test.php> (MAMP: <http://localhost:8888/test.php>).
4. You should see **PHP is working!** If you see the code itself instead, check that Apache is running and that you used `http://localhost/...` and didn't double-click the file.

---

## Step 5: Get the lab files

You will make your **own copy** (a "fork") of the class repository on GitHub, then download it (a "clone") into your htdocs folder.

### 5a. Fork the class repository

1. Open the class repository: <https://github.com/tony0520/web-programming-lab-2026>
2. Click **Fork** (top right), then **Create fork**.
3. You now have your own copy at `github.com/YOUR-USERNAME/web-programming-lab-2026`.

### 5b. Clone your fork with VS Code

1. Open VS Code. Close any open folder (**File → Close Folder**).
2. Press **Ctrl + Shift + P** (Windows) or **Cmd + Shift + P** (Mac), type **Git: Clone** and press Enter.
3. Choose **Clone from GitHub**. Your browser opens. Sign in to GitHub and click **Authorize**.
4. Pick **YOUR-USERNAME/web-programming-lab-2026** from the list.
5. When asked where to save it, choose your **htdocs** folder.
6. Click **Open** when VS Code asks.

<details>
<summary>Prefer the command line?</summary>

```bash
cd C:/xampp/htdocs
```

(macOS: `cd /Applications/XAMPP/xamppfiles/htdocs`, or `cd /Applications/MAMP/htdocs` for MAMP)

```bash
git clone https://github.com/YOUR-USERNAME/web-programming-lab-2026.git
```
</details>

> **macOS "permission denied" when cloning into htdocs?** Run this in Terminal (it asks for your Mac password), then try again:
> ```bash
> sudo chown -R "$USER" /Applications/XAMPP/xamppfiles/htdocs
> ```

### 5c. Check it worked

With Apache running, visit:
<http://localhost/web-programming-lab-2026/class-01/starter/> (MAMP: add `:8888` after `localhost`)

You should see a plain page with all the text squashed onto one line. It's supposed to look unfinished. That's our Class 1 job!

---

## Step 6: Final checklist

Tick everything before Class 1:

- [ ] I have a GitHub account and know my username
- [ ] VS Code opens, with **Live Server**, **Prettier** and **PHP Intelephense** installed
- [ ] Auto Save is on
- [ ] `git --version` shows a version number
- [ ] `git config --global --list` shows my name and email
- [ ] Apache and MySQL start (green / Running)
- [ ] <http://localhost/test.php> shows "PHP is working!"
- [ ] I forked and cloned the lab repository into htdocs, and the Class 1 starter page opens

---

## Troubleshooting

| Problem | Fix |
|---|---|
| **Apache won't start (Windows)**: "Port 80 in use" | Another program is using port 80 (often Skype, IIS or VMware). In the XAMPP Control Panel, click **Config** next to Apache → **httpd.conf**. Change `Listen 80` to `Listen 8080` and `ServerName localhost:80` to `ServerName localhost:8080`. Save, start Apache again, and use <http://localhost:8080> from now on. |
| **Apache won't start (macOS)** | macOS may have its own web server running. In Terminal run `sudo apachectl stop`, then try again. Still stuck? Use MAMP. |
| **MySQL won't start**: "Port 3306 in use" | You may already have MySQL installed. Stop that MySQL service, or tell your demonstrator. |
| **MySQL "shutdown unexpectedly"** | **Don't delete anything.** Tell your demonstrator. There's a safe fix. |
| **"This site can't be reached" on localhost** | Apache isn't running. Start it in XAMPP / MAMP. |
| **The browser shows my PHP code instead of running it** | You opened the file directly (the address starts with `file:///`). Use `http://localhost/...` instead. |
| **My file is called `index.html.txt`** | Do Step 0, then rename the file. |
| **"Clone from GitHub" doesn't show my repositories** | Make sure you completed the browser sign-in and clicked **Authorize**. You can also paste the URL: `https://github.com/YOUR-USERNAME/web-programming-lab-2026.git` |
