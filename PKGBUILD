pkgname=craftbukkit-snapshot
pkgver=1.4.6r0.3
pkgrel=1
pkgdesc="Minecraft server implementing the Bukkit API (snapshot)"
arch=(any)
url="http://bukkit.org"
license=("LGPL")
depends=(java-runtime tmux)
conflicts=(bukkit craftbukkit craftbukkit-git)
provides=(bukkit "craftbukkit=1.4.5r1.0-2")
source=("http://cbukk.it/craftbukkit-beta.jar"
"craftbukkit.service"
"craftbukkit.sh")
noextract=("craftbukkit-beta.jar")
md5sums=('f365fd074c795c227d449eaebcddc086'
         '0ba6b038ca1b04ef1e4f2746e3011a71'
         'ce316df76d7bb3546d1c4ab8c762f9dd')

package() {
  install -Dm644 "$srcdir/craftbukkit-beta.jar" "$pkgdir/srv/craftbukkit/craftbukkit.jar"
  install -m755 "$srcdir/craftbukkit.sh" "$pkgdir/srv/craftbukkit/craftbukkit.sh"
  install -Dm644 "$srcdir/craftbukkit.service" "$pkgdir/usr/lib/systemd/system/craftbukkit.service"
}

# vim:set ts=2 sw=2 et:
