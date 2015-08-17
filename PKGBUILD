# $Id: PKGBUILD 95993 2013-08-19 09:47:23Z angvp $
# Maintainer: Balló György <ballogyor+arch at gmail dot com>

_pkgname=configglue
pkgname=python2-$_pkgname
pkgver=1.1.2
pkgrel=2
pkgdesc="Library that glues together python's optparse.OptionParser and ConfigParser.ConfigParser"
arch=('any')
url="https://launchpad.net/configglue"
license=('BSD')
depends=('python2-xdg')
makedepends=('python2-setuptools')
source=(http://launchpad.net/$_pkgname/trunk/$pkgver/+download/$_pkgname-$pkgver.tar.gz)
md5sums=('9ad83551a2cb4cf20cbe936c9f80bd1e')

build() {
  cd "$srcdir/$_pkgname-$pkgver"

  python2 setup.py build
}

check() {
  cd "$srcdir/$_pkgname-$pkgver"

  python2 setup.py test
}

package() {
  cd "$srcdir/$_pkgname-$pkgver"

  python2 setup.py install --root=$pkgdir/ --optimize=1

  install -Dm644 LICENSE "$pkgdir/usr/share/licenses/$pkgname/LICENSE"
}
