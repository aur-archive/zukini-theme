# Mantainer: Diego <cdprincipeat gmaildot com>
# Contributor: grimi <grimi at poczta dot fm>

pkgname=zukini-theme
pkgver=20120817
pkgrel=2
pkgdesc="A gtk2, gtk3, metacity, gnome-shell and unity theme..."
arch=('any')
url="http://gnome-look.org/content/show.php/Zukini?content=147431"
license=('GPL')
depends=('gtk-engines' 'gtk-engine-murrine' 'gtk-engine-unico>=1.0.2')
source=("${pkgname}-${pkgver}.zip::http://gnome-look.org/CONTENT/content-files/147431-Zukini.zip"
        "openbox-themerc")
md5sums=('0c4804ab7f4d04ac065d04c2bf855d73'
         'd6b5f5a302b13b23fe92463f9104dd2e')


package() {
  # fix xfce panel
  sed '/Xfce/s/\(theme-panel\)/\1-light/' -i Zukini/gtk-2.0/widgets/panel.rc

  # install theme
  find Zukini/ -type f \
      -exec install -Dm644 "{}" "$pkgdir/usr/share/themes/{}" \;

  # openbox
  install -Dm644 openbox-themerc \
      "$pkgdir/usr/share/themes/Zukini/openbox-3/themerc"
}

# vim:set ts=2 sw=2 et:
