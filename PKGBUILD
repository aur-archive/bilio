# Maintainer: Jean-Noël Rouchon <mail@mithril.re>

pkgname=bilio
pkgver=0.5.2
pkgrel=1
pkgdesc="Logiciel de gestion commerciale"
arch=('any')
url="http://bilio.org"
license=('GPL3')
depends=('ruby' 
				 'postgresql-libs' 
				 'ruby-activerecord'
				 'ruby-gtk3'
				 'ruby-bcrypt'
				 'ruby-prawn'
				 'ruby-ezcrypto'
				 'ruby-pg'
				 'sane'
				 'imagemagick'
				 )
options=()

source=('http://public.mithril.re/bilio/bilio-0.5.2.tar.gz')
md5sums=('ac98889e7fc0dfdb31967743357cbcd5')

package() {
  cd ${srcdir}/$pkgname-$pkgver
  install -D -m755 bilio $pkgdir/usr/bin/bilio
  install -D -m755 bilio.desktop $pkgdir/usr/share/applications/bilio.desktop
  install -dm755 $pkgdir/usr/share/$pkgname/src/resources/articles
  install -dm755 $pkgdir/usr/share/$pkgname/src/resources/icons
  install -dm755 $pkgdir/usr/share/$pkgname/db/migrate
  install -D -m644 Rakefile $pkgdir/usr/share/$pkgname/
  install -D -m644 src/*.* $pkgdir/usr/share/$pkgname/src/
  install -D -m644 src/resources/icons/*.* $pkgdir/usr/share/$pkgname/src/resources/icons/
  install -D -m644 db/*.* $pkgdir/usr/share/$pkgname/db/
  install -D -m644 db/migrate/*.* $pkgdir/usr/share/$pkgname/db/migrate/
  install -D -m644 LICENCE $pkgdir/usr/share/$pkgname/
}
