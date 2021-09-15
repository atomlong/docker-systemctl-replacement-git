# Maintainer: Gore Liu <goreliu@126.com>
# Contributor: Atom Long <atom.long@hotmail.com>

pkgname=docker-systemctl-replacement-git
_pkgname=docker-systemctl-replacement
pkgver=1883.9cbe1a0
pkgrel=1
pkgdesc="docker systemctl replacement"
url='https://github.com/gdraheim/docker-systemctl-replacement'
arch=('any')
license=('GPL')
depends=('python')
source=("${_pkgname}::git+${url}.git")
sha512sums=('SKIP')
install=systemctl.install

pkgver() {
  cd "${srcdir}/${_pkgname}"
  echo "$(git rev-list --count HEAD).$(git rev-parse --short HEAD)"
}

package() {
  cd "${srcdir}/${_pkgname}"
  install -Dm755 "files/docker/systemctl3.py" "${pkgdir}/usr/bin/systemctl.py"
}
