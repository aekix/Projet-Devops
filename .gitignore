package {
'apache2':
  ensure   => present,
}

package {
'php7.3':
  ensure   => present,
  name     => 'php7.3',
  provider => apt
}

file {
'download':
  ensure => present,
  path   => '/usr/src/dokuwiki.tgz'
  source => 'https://download.dokuwiki.org/src/dokuwiki/dokuwiki-stable.tgz',
}

exec {
'unzip':
  command => 'tar xavf dokuwiki.tgz',
  cwd     => '/usr/src',
  path    => ['/usr/bin']
}

file {
'rename':
  ensure => present,
  source => '/usr/src/dokuwiki-2020-07-29',
  path   => '/usr/src/dokuwiki'
}

file {
'rights recettes':
  path   => '/var/www/recettes.wiki',
  recurse => true,
  owner   => 'www-data',
  ensure => directory,
  group   => 'www-data'
}

file {
'rights politique':
  path   => '/var/www/politique.wiki',
  recurse => true,
  ensure => directory,
  owner   => 'www-data',
  group   => 'www-data'
}

file {
'Cp recettes.wiki':
  ensure => present,
  source => '/usr/src/dokuwiki',
  path   => '/var/www/recettes.wiki'
}

file {
'Cp politique.wiki':
  ensure => present,
  source => '/usr/src/dokuwiki',
  path   => '/var/www/politique.wiki'
}
