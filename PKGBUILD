# Maintainer: Arch Haskell Team <arch-haskell@haskell.org>
_hkgname=minirotate
pkgname=minirotate
pkgver=0.1.2.2
pkgrel=2
pkgdesc="Minimalistic file rotation utility"
url="http://hackage.haskell.org/package/${_hkgname}"
license=('custom:BSD3')
arch=('i686' 'x86_64')
makedepends=('ghc' 'haskell-data-accessor=0.2.1.2' 'haskell-data-accessor-template=0.2.1.3' 'haskell-directory=1.0.1.1' 'haskell-filepath=1.1.0.4' 'haskell-mtl>=1.1.0' 'haskell-old-locale=1.0.0.2' 'haskell-old-time=1.0.0.5' 'haskell-process=1.0.1.3' 'haskell-safe=0.2' 'haskell-split=0.1.2' 'haskell-template-haskell=2.4.0.1')
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
    install -D -m644 LICENSE ${pkgdir}/usr/share/licenses/${pkgname}/LICENSE
    rm -f ${pkgdir}/usr/share/doc/${pkgname}/LICENSE
}
md5sums=('50e1bf465443f3ea4c23ef34dbaba8e1')
