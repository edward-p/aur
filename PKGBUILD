# Maintainer:  edward-p <edward AT edward-p DOT xyz>

pkgname=vimrc-git
pkgver=r339.3aefdbd2
pkgrel=1
pkgdesc="The ultimate Vim configuration: vimrc"
arch=('any')
url='https://github.com/amix/vimrc'
license=('MIT')
depends=('vim')
makedepends=('git')
install=${pkgname}.install
source=("${pkgname}::git+https://github.com/amix/vimrc.git")
sha256sums=('SKIP')

pkgver() {
  cd ${pkgname}
  printf "r%s.%s" "$(git rev-list --count HEAD)" "$(git rev-parse --short HEAD)"

}


package() {
  cd "${srcdir}/${pkgname}"

  mkdir -p "${pkgdir}/usr/share/vimrc"
  install -D -m644 "LICENSE" "${pkgdir}/usr/share/licenses/${pkgname}/LICENSE"
  cp -r * "${pkgdir}/usr/share/vimrc/"

}
