# Maintainer: Arch Haskell Team <arch-haskell@haskell.org>
_hkgname=internetmarke
pkgname=internetmarke
pkgver=0.0.2
pkgrel=3
pkgdesc="Shell command for constructing custom stamps for German Post"
url="http://hackage.haskell.org/package/${_hkgname}"
license=('GPL')
arch=('i686' 'x86_64')
makedepends=('ghc' 'haskell-hpdf<1.5' 'haskell-explicit-exception<0.1' 'haskell-mtl<1.2' 'haskell-parsec=2.1.0.1' 'haskell-process=1.0.1.3')
depends=('gmp')
options=('strip')
source=(http://hackage.haskell.org/packages/archive/${_hkgname}/${pkgver}/${_hkgname}-${pkgver}.tar.gz)
build() {
    cd ${srcdir}/${_hkgname}-${pkgver}
    runhaskell Setup configure --prefix=/usr --docdir=/usr/share/doc/${pkgname} -O
    runhaskell Setup build
}
package() {
    cd ${srcdir}/${_hkgname}-${pkgver}
    runhaskell Setup copy --destdir=${pkgdir}
}
md5sums=('064b53432b9953942391d5fd7806ed1e')
