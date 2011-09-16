# Maintainer: Martin Panter <vadmium à gmail·com>
_name=dir
pkgname="mkinitcpio-$_name"
pkgver=0.1.0
pkgrel=0
pkgdesc="Initcpio hook to mount a subdirectory as the root file system"
url="https://bbs.archlinux.org/viewtopic.php?pid=932362#p932362"
arch=(any)
license=("custom:Public domain")
source=(README.txt hook install)
md5sums=(
  fd9f2f39e08838f24bb23a32750b999b
  3ff39deb52dc7379b8509f388602df93
  2e66d470b1ab50cf1dce778356c68599
)

package() {
  local DEST=(
    "usr/share/doc/$pkgname/README.txt"
    "lib/initcpio/hooks/$_name"
    "lib/initcpio/install/$_name"
  )
  for((i = 0; i < "${#source[@]}"; ++i)); do
    mkdir -p "$pkgdir/$(dirname "${DEST[i]}")"
    install --mode +r "$srcdir/${source[i]}" "$pkgdir/${DEST[i]}"
  done
}
