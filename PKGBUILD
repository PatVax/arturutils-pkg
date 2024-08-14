# Maintainer: Alad Wenter <https://github.com/AladW>
pkgname=arturutils
pkgver=19.9
pkgrel=1
pkgdesc='helper tools for the arch user repository'
url='https://github.com/AladW/aurutils'
arch=('any')
license=('custom:ISC')
source=('git+https://github.com/PatVax/arturutils.git#branch=Testing')
changelog=aurutils.changelog
sha256sums=('SKIP')
conflicts=('aurutils' 'aurutils-git' 'arturutils-git')
provides=("arturutils=${pkgver%%.r*}")
depends=('git' 'pacutils' 'curl' 'bash' 'perl' 'perl-json-xs')
makedepends=('git')
optdepends=('bash-completion: bash completion'
            'zsh: zsh completion'
            'artools: aur-chroot'
            'vifm: default pager'
            'ninja: aur-sync ninja support'
            'bat: view-delta example script'
            'git-delta: view-delta example script'
            'python-srcinfo: sync-rebuild example script')

build() {
    cd arturutils
    make
}

package() {
    cd arturutils
    make DESTDIR="$pkgdir" install
}
