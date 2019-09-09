# Maintainer: Jan Boelsche <jan@lagomorph.de>
pkgname=tre-deployment-find
pkgver=1.1.0
pkgrel=1
pkgdesc="find previously deployed webapps and system images"
arch=('any')
url=""
license=('MIT')
groups=()
depends=(
  'nodejs'
)

makedepends=('npm')
checkdepends=()
optdepends=()
provides=()
conflicts=()
replaces=()
source=()

pkgver () {
  npm view ${pkgname}@latest version
}

package () {
  source "$HOME/.nvm/nvm.sh"
  nvm use 10.8.0
  local _npmdir="${pkgdir}/usr/lib/node_modules/"
  mkdir -p $_npmdir
  npm install -g --prefix "${pkgdir}/usr" ${pkgname}@${pkgver}
}
