# Maintainer: Bouteiller a2n Alan <a2n.dev@pm.me>

_pkgname=blurredwallpaper
_plasmoidName="a2n.blur"
pkgname=plasma6-wallpapers-blurredwallpaper-git
pkgver=3.2.0
pkgrel=3
pkgdesc="KDE Plasma wallpaper plugin that blurs the wallpaper when a window is active"
arch=(x86_64)
url="https://github.com/bouteillerAlan/${_pkgname}"
license=(GPL-3.0-or-later)
makedepends=('git')
depends=('plasma-workspace')
provides=("$_pkgname=$pkgver")
conflicts=('plasma6-wallpapers-blurredwallpaper')
source=("git+${url}.git")
md5sums=("SKIP")
validpgpkeys=(6A2ECC8A396F8A943A109A1E0F11C2A6BF79111E)

package() {
    cd "$srcdir/${_pkgname}"
    install -Dm 644 LICENSE -t "${pkgdir}"/usr/share/licenses/"${pkgname}"/
    find "${_plasmoidName}" -type f -exec install -Dm 644 "{}" "${pkgdir}/usr/share/plasma/wallpapers/{}" \;
}

