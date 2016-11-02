# Maintainer: zandi <the.zandi@gmail.com>

# NOTE: the rpm has a version file in it, but this doesn't match the version of the package.
# Maybe later we can use the pkgver() function to fix this :/
pkgname=semaphor
pkgver=1.1.7
pkgrel=1
epoch=
pkgdesc="Client for SpiderOak's chat and collaboration tool providing end-to-end cryptography"
arch=('x86_64')
url="https://spideroak.com/solutions/semaphor"
license=('custom')
groups=()
depends=('libsodium' 'gtk2' 'alsa-lib' 'libnotify' 'gconf' 'libxtst' 'nss')
makedepends=()
checkdepends=()
optdepends=()
provides=()
conflicts=()
replaces=()
backup=()
options=()
install=
changelog=
# spideroak doesn't give us a url w/ the version in it, it just feeds us the (probably) latest...
source=("${pkgname}-${pkgver}-${arch}.rpm::https://spideroak.com/releases/semaphor/linux")
noextract=()
sha256sums=('ed5b8060ea872e819bd113c263e9916e6f45f6715732730696deb3e030e04107') # keep updated manually
validpgpkeys=()

package() {
	cp -R "${srcdir}/usr" "${pkgdir}"
	mkdir -p "${pkgdir}/usr/share/licenses/semaphor"
	cp "${srcdir}/usr/share/semaphor/LICENSE" "${pkgdir}/usr/share/licenses/semaphor/LICENSE"
}
