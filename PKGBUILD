# Maintainer: Nikoloz Shvelidze <shveloo@gmail.com>
pkgname=chronicler-bin
pkgver=0.50.0
pkgrel=2
pkgdesc="The free offline worldbuilding tool for writers and GMs."
arch=('x86_64')
license=('PolyForm-Shield-1.0.0')
depends=('webkit2gtk-4.1' 'gtk3')
provides=("chronicler")
conflicts=("chronicler")
url="https://github.com/mak-kirkland/chronicler"
source=(
    "https://github.com/mak-kirkland/chronicler/releases/download/v${pkgver}-alpha/Chronicler_${pkgver}_amd64.deb"
    "https://raw.githubusercontent.com/mak-kirkland/chronicler/v${pkgver}-alpha/LICENSE"
)
sha256sums=('040f363d91f7720de5672c356ceaddfd225e4b0af28681c68d104a6b81600a0d'
            '4b4b7f846a2a8865f82a40eb0c475f534c9c044bd202536ad35e1060bd27dc5d')

prepare() {
    ar x Chronicler_${pkgver}_amd64.deb
}

package() {
    mkdir -p "${pkgdir}/usr/share/licenses/${pkgname}"
    install -Dm644 $srcdir/LICENSE -t "${pkgdir}/usr/share/licenses/${pkgname}/"
    tar xzf $srcdir/data.tar.gz -C $pkgdir
}
