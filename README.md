## 📦 How to Install Custom XBPS Packages

### Download and Install

You cannot install an `.xbps` file directly; you must index it first. Replace the URL below with the one from your specific Release.

```bash
# 1. 📥 Fast Install
curl -LO <release_url>
xbps-rindex -a *.xbps
sudo xbps-install -R . <package_name>

# 2. Download the package(Example)
curl -LO https://github.com/Ackerman-00/void-template/releases/download/latest-protonplus/protonplus-0.5.14_1.x86_64.xbps

# 3. Index the file to create a local repository(Example)
xbps-rindex -a protonplus-0.5.14_1.x86_64.xbps

# 4. Install the package using the current directory (-R .) as a repo(Example)
sudo xbps-install -R . protonplus
```

---

### A Quick Tip

Since filenames change when versions update (e.g., `0.5.14` becomes `0.5.15`), you can use **wildcards** to make the commands easier:

```bash
xbps-rindex -a *.xbps
sudo xbps-install -R . protonplus

```
