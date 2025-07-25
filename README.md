# ImgScene

ImgScene is a lightweight tool to arrange, transform, and save scenes made from multiple images.

You can use it to:

- **Move**, **rotate**, **flip**, and **layer** images

- Create masking **paths** using nodes

- **Save** and **reload** your scenes using a **.isc** file (simple **JSON**)

- This repository includes binaries for **macOS**, **Linux**, and **Windows**.

---

## Installing


### macOS

1 - Install dependencies using [Homebrew](https://brew.sh):
```bash
brew install glfw
brew install glew
```

2 - Download and install ImgScene
```bash
curl -L https://github.com/Siamaster/ImgScene-Public/raw/master/mac/ImgScene.zip -o /tmp/ImgScene.zip && \
unzip -oq /tmp/ImgScene.zip -d /tmp && \
mv -f /tmp/cmake-build-debug/ImgScene.app /Applications/ && \
rm -rf /tmp/cmake-build-debug /tmp/ImgScene.zip && \
xattr -dr com.apple.quarantine /Applications/ImgScene.app
```

### linux

```bash
sudo bash -c 'curl -L -o /tmp/imgscene.deb "https://raw.githubusercontent.com/Siamaster/ImgScene-Public/master/linux/ImgScene.deb" && apt install -y /tmp/imgscene.deb || apt --fix-broken install -y && rm /tmp/imgscene.deb'
```

### Windows

No dependencies needed. Just run **ImgScene.exe**.

## Manual / Usage

### Supported file formats
You can open the following file types:

- **Images:** `*.jpg`, `*.jpeg`, `*.png`, `*.bmp`
- **Scene files:** `*.json`, `*.isc`

`.isc` files are json files.

### Open files

- **Drag & drop**
- **Ctrl + O**

### Save files
- **Ctrl + S**
- **Ctrl + Shift + S**  (Save As)

### Reload scene
- **Ctrl + R**

### Fullscreen
- **F2** -> Toggle
- **Esc** -> Exit

### Browse image folders

- **[←] [→]** - Works only if you haven't transformed the image
- **Ctrl + [←] [→]** - Works always, keeps transformations

### Select image and bring them to front

- **🖱L**

### Deselect

- **🖱R**
- **Q**

### Remove

- **Delete**

### Select multiple images

- **Ctrl + 🖱L**

### Move frames and paths

- **Ctrl + 🖱️L drag**
- **🖱L + 🖱R drag**

### Pan/scroll image / resize frames / move node/smooth node handle

- **🖱️L drag**

### Zoom images

- **🖱Wheel**
- **＋/－** -> finer control

### Rotate images

- **R + 🖱L drag**

### Flip images

- **F**

### Lock z-indices

- **L** -> Toggle

### Use paths

- **P** -> Toggle
- **Ctrl + Shift + F** -> Reset path to frame bounds

### Insert smooth node

- **2x🖱L**
- **1 + 2x🖱L** -> Cusp

### Select nodes

- **Ctrl + 🖱L** -> Toggle
- **Shift + 🖱L** -> Select all in path
- **Ctrl + A** -> Select all in all paths

### Auto smooth (all selected smooth nodes)

- **S**
- **Alt + S** -> Auto smooth all smooth nodes in all selected paths

### Convert to cusp/smooth node

- **1** -> Cusp
- **2** -> Smooth