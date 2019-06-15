pkgname=archlinux-sys-config
pkgver=r1.1a13bbf
pkgrel=1
pkgdesc="Common Arch Linux system configuration bits"
url="https://github.com/amezin/archlinux-sys-config"
arch=('any')
license=('GPL')
source=("$pkgname::git+file://$(git rev-parse --show-toplevel)#commit=$(git rev-parse HEAD)")
backup=($(find etc/ -type f))
md5sums=('SKIP')

pkgver() {
  cd "$pkgname"
  printf "r%s.%s" "$(git rev-list --count HEAD)" "$(git rev-parse --short HEAD)"
}

package() {
  cd $pkgname
  cp -r etc "${pkgdir}/etc"
}
