# ##################################################
# kicad-10.0.6-x86_64.AppImage
# ##################################################

# Pfad
/var/lib/flatpak/exports/share/applications

# Copy
sudo cp kicad-10.0.6-x86_64.AppImage /var/lib/flatpak/exports/share/applications

# Symbol anlegen
nano ~/.local/share/applications/kicad.desktop

# Symbol ablegen unter (Option 1)
~~.local/share/applications/org.kicad.KiCad~~
/usr/share/icons/hicolor/ XXxXX /apps/

# Symbol ablegen einfach (Option 2) mit Refresh Icon cache
sudo mkdir -p /usr/share/icons/hicolor/48x48/apps/kicad
sudo cp org.kicad.KiCad*.svg /usr/share/icons/hicolor/48x48/apps/kicad/
sudo gtk-update-icon-cache -f -t /usr/share/icons/hicolor

Flatpack Icon Pfad (10.0.0)
/var/lib/flatpak/app/org.kicad.KiCad/current/active/export/share/icons/hicolor/scalable/apps

nano ~/.local/share/applications/kicad.desktop

# ########## ~/.local/share/applications/kicad.desktop ##########
[Desktop Entry]
Name=KiCad 10.0.6 (AppImage)
Exec=/var/lib/flatpak/exports/share/applications/kicad-10.0.6-x86_64.AppImage
Icon=/usr/share/icons/hicolor/48x48/apps/kicad/org.kicad.KiCad.svg
Type=Application
Categories=Development;Electronics;
# ########## end ##########

# Ausführbar machen
chmod +x ~/.local/share/applications/kicad.desktop
