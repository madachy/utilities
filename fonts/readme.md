✅ Steps to Use Segoe UI Emoji in Google Colab
1. Upload the Font
```
from google.colab import files
uploaded = files.upload()  # Upload seguiemj.ttf
```
After uploading, suppose the file is called seguiemj.ttf.

2. Install the Font in the Colab Runtime
```
!mkdir -p ~/.fonts
!mv seguiemj.ttf ~/.fonts/
!fc-cache -f -v
```
3. Verify It's Installed
```
!fc-list | grep -i "Segoe UI Emoji"
```
This should return a line showing the font path.

✅ Use in Matplotlib (for preview):
```
import matplotlib.pyplot as plt

plt.figure(figsize=(6, 2))
plt.text(0.5, 0.5, '🔋 ⚡ 🏠 🔘', 
         fontsize=30, 
         fontname='Segoe UI Emoji', 
         ha='center', va='center')
plt.axis('off')
plt.show()
```

✅ Use in Graphviz
You can now safely use:
```
<FONT FACE="Segoe UI Emoji">⚡</FONT>
```
in your HTML-style Graphviz labels.fonts
