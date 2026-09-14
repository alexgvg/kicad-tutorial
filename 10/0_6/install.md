kicad-10.0.6-x86_64.AppImage

# Pfad
/var/lib/flatpak/exports/share/applications

# Copy
sudo cp kicad-10.0.6-x86_64.AppImage /var/lib/flatpak/exports/share/applications

# Symbol anlegen
nano ~/.local/share/applications/kicad.desktop

# ########## ~/.local/share/applications/kicad.desktop ##########
[Desktop Entry]
Name=KiCad 10.0.6 (AppImage)
Exec=/var/lib/flatpak/exports/share/applications/kicad-10.0.6-x86_64.AppImage
Icon=kicad
Type=Application
Categories=Development;Electronics;
# ########## end ##########

# Ausführbar machen
chmod +x ~/.local/share/applications/kicad.desktop
