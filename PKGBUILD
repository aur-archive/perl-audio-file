# PKGBUILD generated by pacpan
pkgname=perl-audio-file
pkgver=0.11
pkgrel=1
pkgdesc="Perl/CPAN Audio::File audio file abstraction library"
arch=(any)
license=(GPL)
url="http://search.cpan.org/~flora/Audio-File-0.11/lib/Audio/File.pm"
depends=('perl-mp3-info' 'perl-mp3-tag' 'perl-ogg-vorbis-header-pureperl' 'perl-audio-flac-header')
options=(!emptydirs)
source=(http://search.cpan.org/CPAN/authors/id/F/FL/FLORA/Audio-File-$pkgver.tar.gz)
md5sums=('d5192657904c812f10ffc302ee7e2228')

build() {
  cd "${srcdir}/Audio-File-${pkgver}"

  # install module in vendor directories.
  PERL_MM_USE_DEFAULT=1 perl Makefile.PL INSTALLDIRS=vendor || return 1
  make  || return 1
  make install DESTDIR=${pkgdir} || return 1

  # remove perllocal.pod and .packlist
  find ${pkgdir} -name perllocal.pod -delete
  find ${pkgdir} -name .packlist -delete
}
# END OF PACPAN PKGBUILD

