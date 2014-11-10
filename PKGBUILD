# Maintainer: sten_gun <robenfi@gmail.com>

pkgname=genlog-git
pkgver=r2.g41a1d85
pkgrel=1
pkgdesc="Bash script that generates logs and creates a paste2.org link, useful when posting on support forums and helps addressing common problems on a GNU/Linux machine."
arch=('any')
url="https://gitorious.org/genlog"
license=('GPL3')
makedepends=('git')
depends=('bash')
provides=('genlog')
source=("${pkgname/-git}::git+https://gitorious.org/genlog/genlog.git")
md5sums=('SKIP')

pkgver() {
  cd "${pkgname/-git}"
  printf "r%s.g%s" "$(git rev-list --count HEAD)" "$(git rev-parse --short HEAD)"
}

package() {
  install -D -m755  "${pkgname/-git}/genlog.sh" "${pkgdir}/usr/bin/genlog"
}
