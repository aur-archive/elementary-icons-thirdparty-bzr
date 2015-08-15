# Maintainer: Maxime Gauduin <alucryd@archlinux.org>

pkgname=elementary-icons-thirdparty-bzr
pkgver=r8
pkgrel=1
pkgdesc="Thirdparty icons for the elementary icon theme"
arch=('any')
url='https://launchpad.net/elementary-community/elementary-thirdparty-icons'
license=('GPL3')
depends=('elementary-icon-theme')
makedepends=('bzr')
provides=("${pkgname%-*}")
conflicts=("${pkgname%-*}")
options=('!emptydirs')
install="${pkgname%-*}.install"
source=("${pkgname%-*}::bzr+http://bazaar.launchpad.net/~versable/elementary-community/elementary-thirdparty-icons/")
sha256sums=('SKIP')

pkgver() {
  cd ${pkgname%-*}

  printf "r%s" "$(bzr revno)"
}

package() {
  cd ${pkgname%-*}

  install -dm 755 "${pkgdir}"/usr/share
  cp -dr --no-preserve=ownership icons/elementary "${pkgdir}"/usr/share/
}

# vim: ts=2 sw=2 et:

