# Maintainer: Arch Haskell Team <arch-haskell@haskell.org>
_hkgname=timberc
pkgname=timberc
pkgver=1.0.3
pkgrel=3
pkgdesc="The Timber Compiler."
url="http://hackage.haskell.org/package/${_hkgname}"
license=('custom:BSD3')
arch=('i686' 'x86_64')
makedepends=('ghc' 'haskell-array=0.3.0.1' 'haskell-binary>=0.4.2' 'haskell-bytestring=0.9.1.7' 'haskell-bzlib>=0.4.0.0' 'haskell-filepath=1.1.0.4' 'haskell-haskell98=1.0.1.1' 'haskell-mtl>=1.1' 'haskell-pretty=1.0.1.1' 'happy>=1.18')
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
md5sums=('83ca478730189f2324eb0b8e17f874a8')
