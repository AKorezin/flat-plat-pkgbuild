pkgname=flatplat-theme
epoch=1
pkgver=3.22.20161109
pkgrel=2
pkgdesc="A Material Design-like flat theme for GTK3, GTK2, Metacity, and GNOME-Shell. This package does not contain chrome skin extension."
arch=('any')
url="https://github.com/nana-4/Flat-Plat"
license=('GPL')
depends=('gtk3>=3.22','gtk-engine-murrine', 'gnome-themes-standard')
optdepends=()
provides=('flatplat-theme')
conflicts=('flatplat-theme-git')
replaces=()
source=("https://github.com/nana-4/Flat-Plat/releases/download/v${pkgver}/Flat-Plat-${pkgver}.tar.gz"
        "https://github.com/nana-4/Flat-Plat/releases/download/v${pkgver}/Flat-Plat-light-${pkgver}.tar.gz")
sha256sums=('77d335d1a946999389e0ffe3418be41df24615b402aaedc1c04fb8ab44468636'
            'baf49e4ec92b585bb2d6e86073395d948e0820725bc9f3a32bb6e415d212a106')

package() {
  cd "Flat-Plat"
  install -dm 755 "${pkgdir}"/usr/share/themes/Flat-Plat
  rm -rf chrome img
  cp -dr --no-preserve='ownership,mode' * "${pkgdir}"/usr/share/themes/Flat-Plat
  cd ..
  cd "Flat-Plat-light"
  install -dm 755 "${pkgdir}"/usr/share/themes/Flat-Plat-light
  rm -rf chrome img
  cp -dr --no-preserve='ownership,mode' * "${pkgdir}"/usr/share/themes/Flat-Plat-light
}
