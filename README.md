## 📦 How to Install Custom XBPS Packages

### Download and Install

You cannot install an `.xbps` file directly; you must index it first. Replace the URL below with the one from your specific Release.

```bash
# 1. Download the package
curl -LO https://github.com/Ackerman-00/void-template/releases/download/latest-protonplus/protonplus-0.5.14_1.x86_64.xbps

# 2. Index the file to create a local repository
xbps-rindex -a protonplus-0.5.14_1.x86_64.xbps

# 3. Install the package using the current directory (-R .) as a repo
sudo xbps-install -R . protonplus

```

---

### A Quick Tip

Since filenames change when versions update (e.g., `0.5.14` becomes `0.5.15`), you can use **wildcards** to make the commands easier:

```bash
xbps-rindex -a *.xbps
sudo xbps-install -R . protonplus

```
