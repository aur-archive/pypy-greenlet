# $Id: PKGBUILD 70305 2012-05-04 08:21:08Z mtorromeo $
# Maintainer: Massimiliano Torromeo <massimiliano.torromeo@gmail.com>
# Maintainer: Felix Yan <felixonmars@gmail.com>
# Contributor: Ralf Schmitt <ralf@systemexit.de>
# Contributor: Krzysztof Malinowski <boromil@gmail.com>

pkgname=pypy-greenlet
pkgver=0.4.0
pkgrel=1
pkgdesc="python coroutine library"
license=("MIT")
url="http://pypi.python.org/pypi/greenlet"
depends=('pypy')
source=(http://pypi.python.org/packages/source/g/greenlet/greenlet-$pkgver.zip)
arch=('i686' 'x86_64')

build() {
	cd "$srcdir/greenlet-$pkgver"
	pypy setup.py build
}

package() {
	cd "$srcdir/greenlet-$pkgver"
	pypy setup.py install --root="$pkgdir"
	install -Dm0644 LICENSE.PSF "$pkgdir/usr/share/licenses/$pkgname/LICENSE.PSF"
}
md5sums=('87887570082caadc08fb1f8671dbed71')
