# Maintainer: kusakata <shohei atmark kusakata period com>

_gemname=fluentd
pkgname=ruby-$_gemname
pkgver=0.10.42
pkgrel=1
pkgdesc="A tool to collect events and logs"
arch=('any')
url="http://fluentd.org/"
license=('Apache')
depends=('ruby' 'ruby-cool.io-1.1' 'ruby-json' 'ruby-http_parser.rb-0.5' 'ruby-msgpack' 'ruby-yajl-ruby')
options=(!emptydirs)
source=("http://rubygems.org/downloads/${_gemname}-${pkgver}.gem")

package() {
	local _gemdir="$(ruby -e'puts Gem.default_dir')"
	gem install --ignore-dependencies --no-user-install --no-ri --no-rdoc -i "$pkgdir/$_gemdir" -n "$pkgdir/usr/bin" $_gemname-$pkgver.gem
	rm "$pkgdir/$_gemdir/cache/$_gemname-$pkgver.gem"
}

md5sums=('644393515051ad585120a737f309f1f8')
