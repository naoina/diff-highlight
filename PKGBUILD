# This is an example PKGBUILD file. Use this as a start to creating your own,
# and remove these comments. For more information, see 'man PKGBUILD'.
# NOTE: Please fill out the license field for your package! If it is unknown,
# then please put 'unknown'.

# See http://wiki.archlinux.org/index.php/Python_Package_Guidelines for more
# information on Python packaging.

# Maintainer: Your Name <youremail@domain.com>
pkgname=diff-highlight
pkgver=1.2.0
pkgrel=1
pkgdesc="pretty diff highlighter; emphasis changed words in diff<Paste>"
arch=('any')
url="https://github.com/tk0miya/diff-highlight"
license=('Apache')
groups=()
depends=('python')
makedepends=('python-setuptools' 'python2-setuptools')
provides=()
conflicts=()
replaces=()
backup=()
options=(!emptydirs)
install=
source=("${pkgname}-${pkgver}.tar.gz::https://github.com/tk0miya/${pkgname}/archive/${pkgver}.tar.gz")
sha512sums=('fc43792f09e271d3624aaea93a5f9827d3101cb8731faaf7c1c3b9bc17bf10ad0505f76d31f11ce574e19af1ff9822f80e0fd9b3d582821305cca30e1512b7fe')

package() {
  cd "${srcdir}/${pkgname}-${pkgver}"
  python setup.py install --root="${pkgdir}/" --optimize=1
  install -Dm 644 LICENSE "${pkgdir}/usr/share/licenses/${pkgname}/LICENSE"
  install -Dm 644 README.rst "${pkgdir}/usr/share/doc/${pkgname}/README"
}

# vim:set ts=2 sw=2 et:
